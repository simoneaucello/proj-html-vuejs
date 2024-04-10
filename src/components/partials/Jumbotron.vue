<script>
  export default {
    
  }
</script>
<template>
  <div class="container-fluid d-flex align-items-center jumbo flex-column">
    <div class="tron container">
    <h1>Tech Forum!</h1>
    <p class="text-white my-4">Discuss all the latest technology news and trends</p>
    <button type="button" class=" my_btn my-4 text-white">GET AVADA NOW! &nbsp;></button>
  </div>
  </div>
</template>


<style lang="scss" scoped>
@use '/src/assets/scss/partials/variables' as *;

.jumbo{
  background-image: url(/public/img/home_slider_bg.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  h1{
    color: $white;
    font-size: 100px;
    font-weight: bold;
  }
  .tron{
    margin-top: 280px;
    margin-bottom: 280px;
    .my_btn{
      background-color: $easternblue;
      padding: 7px 30px;
      border: none;
      &:hover{
        background-color: #202325;
        transition: all .3s ease-out;
      }
    }
  }
}

</style>