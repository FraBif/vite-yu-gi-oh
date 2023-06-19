<script>
    import CardsHolder from './CardsHolder.vue';
    import axios from 'axios';
 
 

    export default{
        name:'CardsList',
        data(){
            return {
                apiUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
                CardsDatabase : [],
                
            }
        },
        components:{
            CardsHolder,
        },

        created(){
            axios.get(this.apiUrl)
            .then( (response) => {
                CardsDatabase.push(response.data.results);
               
            })
            
        }
    }
</script>

<template>
    <div class="container">
        <div class="row py-3 px-5 justify-content-evenly">
            <CardsHolder v-for="character in CardsList"
                :name="character.name"
                :archetype="character.species"
                :status="character.status"
                :image="character.image"
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