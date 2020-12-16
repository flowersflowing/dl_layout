<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
    Layout,
  }
}
</script>

<style lang="scss">
 @import 'node_modules/bootstrap/scss/bootstrap.scss';
</style>
