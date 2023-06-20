<script>
   import CardsList from "../components/CardsList.vue";
   import { store } from "../store"
   

export default {
    name:"AppMain",
    data(){
        return {
            store,
            cardsDatabase: [],
            apiUrl: "https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0"
        }
    },
    components:{
        CardsList
    }
}
</script>

<template>
    <main>
        <CardsList :cardsDatabase="cardsDatabase" />
    </main>
</template>

<style>

</style>