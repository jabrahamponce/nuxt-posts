<template>
  <div :spacing="5" style="margin-bottom: 50px">
    <c-box
      v-for="post in posts"
      :id="post.id"
      :key="post.id"
      shadow="md"
      border-width="1px"
      style="margin-top: 10px"
    >
      <BoxContent
        :title="post.title"
        :subtitle="post.subtitle"
        :done-by-on="post.doneByOn"
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
          title: 'See the Vue',
          subtitle: 'Vue makes front-end development a breeze.',
          doneByOn: 'by Jose Ponce, Jan. 27th, 2020',
          goTo: '/blogpost',
        },
        {
          id: '2',
          title: 'Go Nuxt 1!',
          subtitle: 'Vue makes front-end development a breeze x2',
          doneByOn: 'by Jose Ponce, Jul. 27th, 2020',
          goTo: '/blogpost',
        },
        {
          id: '3',
          title: 'Go Nuxt 2',
          subtitle: 'Vue makes front-end development a breeze x3',
          doneByOn: 'by Jose Ponce, Dec. 27th, 2020',
          goTo: '/blogpost',
        },
      ],
    }
  },
}
</script>

<style scoped></style>
