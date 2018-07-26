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

<style lang="scss">
  html, body {
    height: 100%;
    margin: 0px;
    padding: 0px;
    background-color: #EEEEEE;
  }
  .app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    height: 100%;
    overflow-y: scroll;
  }
</style>
