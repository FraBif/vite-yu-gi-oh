<script>
    import CardsHolder from './CardsHolder.vue';
    import axios from 'axios';
 

    export default{
        name:'CardsList',
        data(){
            return {
                apiUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
                charactersList : [],
                store
            }
        },
        components:{
            CardsHolder,
        },

        created(){
            axios.get(this.apiUrl)
            .then( (response) => {
                console.log(response.data.results);
               
            })
            
        }
    }
</script>

<template>
    <div class="container">

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