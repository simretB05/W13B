<template>
  <div id="app">
  <DisplayPosts></DisplayPosts>
  </div>
</template>

<script>
import DisplayPosts from '@/components/DisplayPosts.vue'
export default {
  name: 'App',
  components: {
    DisplayPosts,
    
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
