<template>
  <div>
    <Nav />
    <div style="text-align: center; width: 70%; margin: 0 auto">
      <c-heading>Newest Posts</c-heading>
      <c-divider />
      <br />
      <div style="text-align: left; width: 80%; margin: 0 auto">
        <c-stack :spacing="5">
          <c-box :p="5" shadow="md" border-width="1px">
            <c-heading>See the Vue</c-heading>
            <c-text font-size="xl" :mt="4"
              >Vue makes front-end development a breeze.</c-text
            >
            <c-text :mt="4">Vue makes front-end development a breeze.</c-text>
          </c-box>
          <c-box :p="5" shadow="md" border-width="1px">
            <c-heading>Go Nuxt!</c-heading>
            <c-text font-size="xl" :mt="4">
              Nuxt makes writing Vue even easier.
            </c-text>
            <c-text :mt="4">Nuxt makes writing Vue even easier.</c-text>
          </c-box>
          <c-box :p="5" shadow="md" border-width="1px">
            <c-heading>Go Nuxt!</c-heading>
            <c-text font-size="xl" :mt="4">
              Nuxt makes writing Vue even easier.
            </c-text>
            <c-text :mt="4">Nuxt makes writing Vue even easier.</c-text>
          </c-box>
        </c-stack>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style></style>
