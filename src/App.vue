<template>
  <div id="app">
    <Header></Header>
    <!--<div id="nav">-->
    <!--<router-link to="/">Home</router-link> |-->
    <!--<router-link to="/about">About</router-link>-->
    <!--</div>-->
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/headbar.vue';
export default {
  components: {
    Header
  }
}
</script>

<style>
  #app {
    background-image: linear-gradient(to top, #a8edea 0%, #fed6e3 100%);
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    min-width: 1408px;
  }
</style>
