<template>
  <CThemeProvider>
    <CReset />
    <Nuxt />
  </CThemeProvider>
</template>

<script>
import { CThemeProvider, CReset } from '@chakra-ui/vue'

export default {
  name: 'DefaultLayout',
  components: {
    CThemeProvider,
    CReset,
  },
}
</script>

<style>
/* body {
  background-color: black;
} */
</style>
