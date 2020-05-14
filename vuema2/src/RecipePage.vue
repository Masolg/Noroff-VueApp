<template>
  <div class="[ row ]">
      <div v-for="recipe in recipes" :key="recipe" class="[ col-sm-12 ]">
          <Recipe v-bind:title="recipe.title"
                  v-bind:url="recipe.href"
                  v-bind:ingredients="recipe.ingredients"
                  v-bind:img="recipe.thumbnail"
          ></Recipe>
      </div>
  </div>
</template>

<script>
import Recipe from './components/Recipe.vue'
export default {
  name: 'RecipePage',
  components:{
      Recipe
  },
  data(){
      return{
          recipes: []
      }
  },
  beforeMount: function(){
      const app = this;
      const conversionUrl = 'https://cors-anywhere.herokuapp.com/';
      const url = 'http://www.recipepuppy.com/api/';

      fetch(conversionUrl + url)
      .then(function(response) {
          return response.json();
      })
      .then(function(result) {
          app.recipes = result.results;
      })
  }
}
</script>

<style>
.row{
    width: 50%;
    margin: auto;
}
</style>
