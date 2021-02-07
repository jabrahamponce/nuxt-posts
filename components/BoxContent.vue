<template>
  <div @click="viewPost">
    <c-heading>{{ title }}</c-heading>
    <c-text font-size="xl" :mt="4">{{ subtitle }}</c-text>
    <c-text :mt="4">{{ doneByOn }}</c-text>
  </div>
</template>

<script>
export default {
  name: '',
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
    doneByOn: {
      type: String,
      required: true,
    },
    // goTo: {
    //   type: String,
    //   required: true,
    // },
  },
  methods: {
    viewPost() {
      this.$router.push('/blogpost')
    },
  },
}
</script>

<style scoped></style>
