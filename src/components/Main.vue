<script>
import Sponsored from './partials/Sponsored.vue'
import Card from './partials/Card.vue'
import {articles} from '../data/articleCards'
import {store} from '../data/store'

  export default {
    components: {
      Card,
      Sponsored
    },


    data(){
      return{
        store,
        // cardItem,
      }
    },

    computed:{

      articleSponsor(){
        return articles.articlesTop
      },

      productSponsor(){
        return articles.articlesBottom
      }
    
    }
  }
</script>


<template>

  <main>
  
  <!-- place to be section  -->
  <div class="container-fluid place-to-be justify-content-center d-flex ">
    <div class="my-5 flex-column text-center forum-text">
      <h6 class="my-5">AVADA FORUM IS THE PLACE TO BE</h6>
      <p class="my-5">In quis lectus sed leo elementum faucibus in dapibus dictum. Nulla molestie tortor nec lectus venenatis, sed blandit dui finibus, dolor at, bibendum purus. Donec vehicula nec tortor ac finibus.
      </p>
    </div>
  </div>
   <!-- place to be section  -->

   <div class="container d-flex justify-content-center flex-column text-center my-5">
    <h6>PHASELLUS EGET METUS</h6>
    <h2>All the latest news</h2>
    <div class="lined my-3"></div>
  </div>

  <!-- cards top  -->
  <div class="container">
    <div class="row row-cols-3  ">    
    <Card 
    class="col d-flex justify-content-center"
    v-for="item in articleSponsor"
    :key="item.id"
    :img="item.img"
    :title="item.title"
    :details="item.details"
    :desc="item.desc"
    />
    <!-- sponsored card  -->
    <Sponsored/>
    <!-- sponsored card  -->
    <Card 
    class="col d-flex justify-content-center"
    v-for="item in productSponsor"
    :key="item.id"
    :img="item.img"
    :title="item.title"
    :details="item.details"
    :desc="item.desc"
    />
  </div>
  <!-- cards top  -->



  


    


  </div>

</main>
</template>



<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.place-to-be{
  background-color: #f1f1f1;
  .forum-text{
    padding: 10px;
  }
  p{
    width: 700px;
    font-size: 20px;
    color: $nevada;
  }
}
h6{
  margin-top: 30px;
}
h2{
  font-size: bold;
}

.lined{
  content: '';
  width: 8%;
  height: 2px;
  border-radius: 3px;
  background-color: #e21b1b;
  margin: 0 auto;
}

</style>