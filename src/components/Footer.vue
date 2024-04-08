<script>
import {store} from '../data/store'
import { footerMenues } from '../data/menues'

  export default {  
    data(){
      return{
        store
      }
    },
    
    computed: {
      popularMenu(){
        return footerMenues.popular
      },
      recentMenu(){
        return footerMenues.recent
      },
      latestMenu(){
        return footerMenues.latest
      },
      socialMenu(){
        return footerMenues.social
      }
    }
  }

</script>


<template>
  <div class="container mb-5 my-5">
    <div class="row row-cols-4 ">
      <div class="col">

        <h5>AVADA TECH FORUM</h5>
        <p class="desc my-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil, accusamus dignissimos sunt facilis nemo sed odio soluta minima vitae, quod consequatur tempora aliquid sapiente et fuga esse. </p>
      </div>

      <!-- col menu  -->
      <div class="col">
        <h5>POPULAR TOPICS</h5>
        <div         
          v-for="(item,index) in popularMenu"
          :key="`h-${index}`"
          class="d-flex foot-desc">
          <span class="my-2">></span>
          <a class=" m-2" :h-ref="item.href">{{item.text}}</a>
        </div>
      </div>
      <!-- col menu  -->
      <!-- col menu  -->
      <div class="col">
        <h5>RECENT TOPICS</h5>
        <div         
          v-for="(item,index) in recentMenu"
          :key="`h-${index}`"
          class="d-flex foot-desc">
          <span class="my-2">></span>
          <a class=" m-2" :h-ref="item.href">{{item.text}}</a>
        </div>
      </div>
      <!-- col menu  -->
      <!-- col menu  -->
      <div class="col">
        <h5>LATEST REPLIES</h5>
        <div         
          v-for="(item,index) in latestMenu"
          :key="`h-${index}`"
          class="d-flex foot-desc">
          <span class="my-2">></span>
          <a class=" m-2" :h-ref="item.href">{{item.text}}</a>
        </div>
      </div>
      <!-- col menu  -->
      
    </div>

  </div>
  <div class="bottom-footer">
    <div class="container d-flex justify-content-between align-items-center my-3">
  
      <p>
        <i class="fa-regular fa-copyright"></i>
        Copyrigth 2012 - 2024 | Avada theme by <span>Theme Fusion</span> All rigth reserved | Powered by <span>Wordpress</span>
      </p>
 

    <div>
      <ul class="d-flex">
        <li>
          <a href="#"><img src="/img/facebook.png" alt=""></a>         
        </li>
        <li>
          <a href="#"><img src="/img/twitter.png" alt=""></a>         
        </li>
        <li>
          <a href="#"><img src="/img/instagram.png" alt=""></a>         
        </li>
        <li>
          <a href="#"><img src="/img/youtube.png" alt=""></a>         
        </li>
       
      </ul>
    </div>

    </div>
  </div>

</template>



<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

h5{
  font-weight: bold;
}
p{
  font-size: 13px;
}
.desc{
  color: $nevada;
}

.foot-desc{
  border-bottom: 1px solid #c0c0c0;
  a{
    text-decoration: none;
    color: $shark;
    cursor: pointer;
    font-size: 13px;
    line-height: 25px;
    font-weight: 600;
  }
}


.bottom-footer{
  border-top: 1px solid #c0c0c0;
  color: $nevada;
  span{
    color: $shark;
    font-weight: bold;
  }
  li{
    list-style: none;
    padding: 5px;
    img{
      width: 30px;
    }
  }
}
</style>