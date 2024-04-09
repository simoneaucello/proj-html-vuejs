<script>
import {featured} from '../../data/sponsored'
  export default {
    props: {
      type: String,
      title: String,
      desc: String
    },



    computed:{
      sponsorProduct(){
        return featured.product
      }
    }
    
  }
</script>

<template>
  <div class="container sponsor text-white">
    <div 
    v-for="(item, index) in sponsorProduct"
    :key="`h-${index}`"
    class="banner">
    <h5>{{item.type}}</h5>
    <h2>{{item.title}}</h2>
    <p class="mt-4">{{item.desc}}</p>
    <button type="button" class="btn my_btn my-4 text-white">READ MORE ></button>
  </div>

  </div>
</template>


<style lang="scss" scoped>
@use '/src/assets/scss/partials/variables' as *;

.sponsor{
  background-image: url(/public/img/featured_article_2_bg.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  margin-bottom: 30px;
  .banner{
    padding: 120px 60px 80px 70px;
    margin: 0 auto;

    .my_btn{
      background-color: $shark;
    }

  }

}

</style>