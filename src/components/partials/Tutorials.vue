<script>
  export default {

    props: {
      id: Number,
      img: String,
      title: String,
      desc: String
    },

    methods: {
      getImagePath(img){
        return new URL(`/public/img/${img}`, import.meta.url).href

      }
    }
    
  }
</script>

<template>
  <div class="tutorial">

    <div class="d-flex mt-3">
      <img :src="getImagePath(`${img}`)" :alt="title">
      <div class="side-text">
      <h6>{{title}}</h6>
      <p>{{desc}}</p>
    </div>
    </div>


  </div>
</template>


<style lang="scss" scoped>
@use '/src/assets/scss/partials/variables' as *;

.tutorial{
  h6, h3{
    font-weight: bold;
  }
 
  .side-text{
    margin-left: 10px;
    p{
      font-size: 13px;
    }

  }
}


</style>