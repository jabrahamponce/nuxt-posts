<template>
  <div class="logo-bg">
    <h1 class="logo">nuxt-posts</h1>
  </div>
</template>

<style>
.logo {
  /* These three properties are where the magic happens: */
  -webkit-text-fill-color: transparent;
  -webkit-text-stroke: 3px hsl(192deg 100% 50%);
  filter: drop-shadow(0px 2px 2px hsl(0deg 0% 0% / 0.5))
    drop-shadow(0px 0px 4px hsl(183deg 100% 50% / 0.5))
    drop-shadow(0px 0px 10px hsl(183deg 100% 50% / 0.5))
    drop-shadow(0px 0px 50px hsl(183deg 100% 50% / 1));

  /* Fallback for IE */
  /* color: rgb(88, 40, 66); */
  /* Misc aesthetic properties */
  font-size: 52px;
  font-weight: 800;
  font-family: 'Helvetica', sans-serif;
}
.logo-bg {
  background-color: black;
}
</style>
