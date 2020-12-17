<template>
  <div id="app">
    <Layout />
  </div>
</template>

<script>
import Layout from './components/Layout.vue'
export default {
  name: 'App',
  components: {
    Layout
  }
}
</script>

<style lang="scss">
 @import 'node_modules/bootstrap/scss/bootstrap.scss';
 @import 'node_modules/bootstrap-vue/src/index.scss';
</style>
