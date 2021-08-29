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
h1 {
  font-size: 3em;
  font-weight: bold;
  margin-bottom: 15px;
}

h2 {
  font-size: 2em;
  font-weight: bold;
}

h3 {
  font-weight: bold;
}

p {
  margin-bottom: 15px;
}
</style>
