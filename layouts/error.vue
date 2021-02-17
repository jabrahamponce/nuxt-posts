<template>
  <div class="error-page">
    <div class="error-page-div">
      <h1 style="font-size: 5em; font-weight: bold">404</h1>
      <h1>Not found. This page can't be displayed.</h1>
      <h1>
        Return to <nuxt-link to="/" style="color: #1acf23">Home</nuxt-link>.
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  name: '',
  components: {},
}
</script>

<style scoped>
.error-page {
  background-color: #1d1b1b;
  height: 100vh;
}
.error-page-div {
  text-align: center;
  padding-top: 10vh;
  font-size: 2em;
  color: #f1f1f1;
}
</style>
