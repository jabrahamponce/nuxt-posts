<template>
  <div>
    <div style="margin: 20px 20px">
      <Nav />
    </div>
    <form id="postForm" @submit.prevent="handleSubmit">
      <h1 style="font-weight: bold; text-align: center; font-size: 2em">
        Submit post
      </h1>
      <h2>Title</h2>
      <input
        v-model="form.title"
        placeholder="Enter blog title"
        name="title"
        required
        style="width: 100%; border: 1px solid black"
      />
      <br /><br />
      <h2>Content</h2>
      <textarea
        v-model="form.message"
        placeholder="Enter blog content"
        name="content"
        required
        style="width: 100%; border: 1px solid black"
        rows="10"
      ></textarea>
      <br />
      <button type="submit">Submit</button>
      <br />
    </form>
    <h2 style="text-align: center">Type Something to Preview</h2>
    <hr />
    <div class="markdown">
      <!-- eslint-disable-next-line vue/no-v-html -->
      <div v-html="compiledMarkdown()"></div>
      <hr />

      <h2 style="text-align: center">Original text - JSON</h2>
      {{ form }}
      <hr />
    </div>
    <div>
      <h2 style="text-align: center; margin-top: 30px">
        How to compile a string directly
      </h2>
      <p>Compile String '# fcdfdf\n## dfdfdfdfd\n### fdfdfdfd'</p>
      <h2 style="text-align: center; margin-top: 30px">Result</h2>
      <div
        v-html="compileString('## fcdfdf\n## dfdfdfdfd\n### fdfdfdfd')"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Admin',
  components: {},
  data() {
    return {
      form: {
        title: '',
        message: '',
      },
    }
  },
  methods: {
    compiledMarkdown() {
      const md = require('markdown-it')()
      const result = md.render(this.form.message)

      //   if (process.client) {
      //     return markdown(this.form.message, { sanitize: true })
      //   }
      return result
    },

    compileString(x) {
      const md = require('markdown-it')()
      const result = md.render(x)
      return result
    },
  },
}
</script>

<style scoped>
#postForm {
  width: 70%;
  margin: 0 auto;
}
</style>
