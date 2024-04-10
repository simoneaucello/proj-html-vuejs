<script>
import {store} from '../data/store'
import {headerMenues} from '../data/menues'
import Jumbotron from '../components/partials/Jumbotron.vue';
  export default {  
    components: {
      Jumbotron
},

    data(){
      return{
        store
      }
    },
    
    computed: {
      mainMenu(){
        return headerMenues.main
      }
    }
  }
</script>


<template>

  <!-- navbar  -->
  <nav class="navbar navbar-expand-lg p-3">
  <div class="container d-flex justify-content-between "> 
    <div>
      <img src="/img/logo.png" alt="logo">
    </div>
    <div>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav d-flex align-items-center">
          <a 
          v-for="(item, index) in mainMenu"
          :key="`h-${index}`"
          class="nav-link m-3" aria-current="page" :href="item.href">{{item.text}}</a>
          <a href="#" class=" join_btn d-flex align-items-center " aria-current="page">JOIN US</a>
          <a href="#" class="nav-link mx-3" aria-current="page"><i class="fa-solid fa-magnifying-glass"></i>
          </a>      
        </div>
      </div>
    </div>
  </div>
</nav>
<!-- navbar  -->

<!-- jumbotron  -->

<Jumbotron />
</template>



<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

nav{
  background-color: $easternblue;
  a{
    color: $white;
    transition: all .3s ease-in;
  }
  .join_btn{
    background-color: black;
    padding: 5px 20px;
    text-decoration: none;
    &:hover{
      color: $easternblue;
      transition: all .5s ease;
  }
  }
}

</style>