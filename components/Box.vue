<template>
  <div :spacing="5" style="margin-bottom: 50px">
    <c-box
      v-for="post in posts"
      :id="post.id"
      :key="post.id"
      shadow="lg"
      border-width="1px"
      padding="10px"
      style="margin-top: 15px"
    >
      <BoxContent
        :title="post.title"
        :subtitle="post.subtitle"
        :done-by-on="post.doneByOn"
        :go-to-post="post.goTo"
      />
    </c-box>
  </div>
</template>

<script>
export default {
  name: '',
  components: {},
  data() {
    return {
      posts: [
        {
          id: '1',
          title: 'See the Vue 1',
          subtitle: 'Vue makes front-end development a breeze.',
          doneByOn: 'by Jose Ponce, Jan. 27th, 2020',
          goTo: '/posts/blogpost-1',
        },
        {
          id: '2',
          title: 'Go Nuxt 2!',
          subtitle: 'Vue makes front-end development a breeze x2',
          doneByOn: 'by Jose Ponce, Jul. 27th, 2020',
          goTo: '/posts/blogpost-2',
        },
        {
          id: '3',
          title: 'Go Nuxt 3',
          subtitle: 'Vue makes front-end development a breeze x3',
          doneByOn: 'by Jose Ponce, Dec. 27th, 2020',
          goTo: '/posts/blogpost-3',
        },
        {
          id: '4',
          title: 'Go Nuxt 4!',
          subtitle: 'Vue makes front-end development a breeze x2',
          doneByOn: 'by Jose Ponce, Jul. 27th, 2020',
          goTo: '/posts/blogpost-2',
        },
        {
          id: '5',
          title: 'Go Nuxt 5',
          subtitle: 'Vue makes front-end development a breeze x3',
          doneByOn: 'by Jose Ponce, Dec. 27th, 2020',
          goTo: '/posts/blogpost-3',
        },
      ],
    }
  },
}
</script>

<style scoped></style>
