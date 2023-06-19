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
    <header>
        <div class="head-container">
             <img src="../assets/img/logo.png" alt="yugi-logo" class="logo">
              <span>
                Yu-Gi-Oh API
              </span>
        </div>
    </header>
    
</template>

<style>
header{
    width: 100%;
    background-color: white;
    display: flex;
    align-items: center ;
    font-size: 2rem;
}

.logo{
    vertical-align: middle;
    width: 100px;
}
</style>
