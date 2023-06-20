<script>
  export default {
    name:"CardsHolder",
    data(){
        return {

        }
    },
    props:{
        name : String,
        archetype : String,
        image : String,
    }
}
</script>

<template>
     <article>
        <img :src="image">
        <div>
            <h5>
                {{ name }} 
            </h5>
            <p class="card-text">
                {{ archetype }} 
            </p>
        </div>
    </article>
</template>

<style>

</style>