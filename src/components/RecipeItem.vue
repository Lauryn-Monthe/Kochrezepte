<template>
    <div class="recipeItemContainer">
        <img class="recipe-image" :src="image"/>
        <div class="right-side">
            <div>
                {{label}}
            </div>
            <div class="bottom-row">
                {{attributes }}
            </div>
        </div>
    </div>
</template>


<script>
    export default {
        name: 'RecipeItem',
        props: {
            image: String,
            label: String,
            attributes: String
        }
    }
</script>


<style scoped>
.recipeItemContainer {
    border: 1px solid rgba(0,0,0,0.2);
    padding: 8px;
    border-radius: 8px;
    margin: 8px;
    display: flex;
    gap: 8px
}
.recipe-image {
    height: 60px;
}

.right-side {
    display: flex;
    flex-direction: column;
    gap: 8px
}

.bottom-row{
    color: rgba(0,0,0,0.4);
    font-size: 12px;
}
</style>