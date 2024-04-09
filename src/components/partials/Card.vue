<script>
  export default {
    props: {
      id: Number,
      img: String,
      title: String,
      details: String,
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
  <div class="container">
    <div class="row">

      <div class="col">
        <div 
        class="my_card">
        <img :src="getImagePath(`${img}`)" :alt="title">
        <h5>{{title}}</h5>
        <span>{{details}}</span>
        <p>{{desc}}</p>
      </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>

</style>