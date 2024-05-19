<template>
    <RecipeItem :image="recipe.image" 
                :attributes="recipe.mealType.join(', ')" 
                :label="recipe.name" 
                v-for="recipe in recipes"/>
</template>


<script>
    import RecipeItem from '../components/RecipeItem.vue';
    import Header from '../components/Header.vue'

    export default {
        components: {
            RecipeItem,
            Header
        },

        data() {
            return {
                recipes: []
            };
        },
        methods: {
            async getRecipes() {
                const query = 'Chicken';
                const url =`https://dummyjson.com/recipes/search?q=${query}`;
                let resp = await fetch(url);
                this.recipes = (await resp.json()).recipes;
                console.log(this.recipes);
            }
        },

        mounted() {
            this.getRecipes();
        },
    }
</script>