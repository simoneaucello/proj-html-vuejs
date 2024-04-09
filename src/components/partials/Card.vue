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
        <h6>{{title}}</h6>
        <span>{{details}}</span>
        <p>{{desc}}</p>
      </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>

.my_card{
  max-width: 302px;
  h6{
    font-weight: bold;
    margin-top: 5px;
  }
  p{
    font-size: 15px;
    margin-top: 10px;
  }
  span{
    font-size: 13px;
  }
}

</style>