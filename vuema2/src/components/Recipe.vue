<template>
    <div class="[ card ]">
        <div class="[ row ]">
            <div class="[ col-sm-4 ]"><img :src="img" /><br /></div>
        </div>
            <div class="[ card--information ]"><br />
                <b>Title: </b>{{title}}<br />
                <b>Ingredients: </b>{{ingredients}}<br />
                <b>Website: </b><a :href="url" target="_blank">Click Here</a><br />
            </div>
    </div>
</template>

<script>
export default {
  name: 'Recipe',
  props: ['title', 'url', 'ingredients', 'img']
}
</script>

<style>
.card{
    border: 1px solid black;
    border-radius: 3px;
    margin: 20px;
    padding: 20px;
}
</style>
