<script>
    import CardsHolder from './CardsHolder.vue';
    import axios from 'axios';
    import store from `../store`
 
 

    export default{
        name:'CardsList',
        data(){
            return {
                apiUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
                CardsDatabase : [],
                store
            }
        },
        components:{
            CardsHolder,
        },

        created(){
            axios.get(this.apiUrl)
            .then( (response) => 
            {this.CardsDatabase = response.data.results;;
               
            })
            
        }
    }
</script>

<template>
    <div class="container">
        <div>
            <CardsHolder v-for="card in CardsDatabase"
                :name="cards.name"
                :archetype="cards.archetype"
                :image="cards.image"
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