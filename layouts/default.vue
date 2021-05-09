<template>
  <transition name="page">
    <Nuxt />
  </transition>
</template>

<style>
html,
body {
  margin: 0;
  padding: 0;
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
}

* {
  box-sizing: border-box;
}

.page-enter {
  /* opacity: 0; */
}

.page-enter-active {
  /* transition: opacity 2s; */
}
</style>
