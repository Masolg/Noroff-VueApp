<template>
  <div id="app">
    <RecipePage />
  </div>
</template>

<script>
import RecipePage from './RecipePage.vue';

export default {
  name: 'App',
  components: {
    RecipePage
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
</style>
