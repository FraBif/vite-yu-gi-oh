<script>
    export default {
        name:'AppHeader',
        data(){
            return {

            }
        }
    }
</script>

<template>
    <div class="head-container">
        <img src="../assets/img/logo.png" alt="yugi-logo" class="logo">
        Yu-gi-Oh API 
    </div>
</template>

<style>
header{
    width: 300px;
}

.logo{
    display: inline-block;
    width: 200px;
}

.head-container{
    display: flex;
    text-align: start;
    align-items: center ;
    font-size: 2rem;
}
</style>
