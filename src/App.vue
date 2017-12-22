<template>
  <div class="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'app',
};
</script>

<style lang="scss" scoped>
  html, body {
    height: 100%;
    margin: 0;
    padding: 0;
  }
  .app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #b3b7bb;
    height: 100%;
    overflow-y: scroll;
  }
</style>
