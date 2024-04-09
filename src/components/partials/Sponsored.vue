<script>
import {featured} from '../../data/sponsored'
  export default {
    props: {
      type: String,
      title: String,
      desc: String
    },



    computed:{
      sponsorArticle(){
        return featured.article
      }
    }
    
  }
</script>

<template>
  <div class="container sponsor text-white">
    <div 
    v-for="(item, index) in sponsorArticle"
    :key="`h-${index}`"
    class="banner">
    <h5>{{item.type}}</h5>
    <h2>{{item.title}}</h2>
    <p class="mt-4">{{item.desc}}</p>
    <button type="button" class="btn my_btn my-4 btn-dark text-white">READ MORE ></button>
  </div>

  </div>
</template>


<style lang="scss" scoped>

.sponsor{
  background-image: url(/public/img/featured_article_1_bg.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  .banner{
    padding: 250px 80px 80px;

  }

}

</style>