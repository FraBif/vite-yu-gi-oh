<script>
    import CardsHolder from "./CardsHolder.vue";
    import { store } from "../store.js";


export default {
    name:'CardsList',
    data(){
        return {
            store
        }
    },
    props:{
        cardsDatabase : Array,
    },
    components:{
        CardsHolder,

    },

}
</script>

<template>
    <div class="container">
        <div>
            <CardsHolder v-for='cards in cardsDatabase'
                :name='cards.name'
                :archetype='cards.archetype'
                :image='cards.image'
            />
        </div>
    </div>
</template>

<style>
 .container{
    margin: auto;
    background-color: white;
    width: 70%;
    height: 90%;
 }
</style>