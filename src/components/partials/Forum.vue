<script>
  export default {
    props: {
      icon: String,
      text: String
    }
    
  }
</script>

<template>
 
        <div class="container">
          <div class="row mt-3 my_container ">
            <div class="col ">
              <div class="my_card mt-4 d-flex justify-content-center align-items-center flex-column">
                <a v-html="icon" class="circle text-white" href="#"></a>
                <h5 class="fw-bold">{{ text }}</h5>
              </div>
            </div>   
          </div>
        </div>

</template>


<style lang="scss" scoped>
@use '/src/assets/scss/partials/variables' as *;

  h2{
    font-size: bold;
  }
 
  .my_card{
    width: 250px;
    height: 250px;
    background-color: #fff;
    border-top: 3px solid $bostonblue;
    cursor: pointer;
    .circle{
      background-color: $salmon;
      padding: 20px;
      border-radius: 50%;
      margin-bottom: 20px;
    }
  }
  .my_container{
    padding: 20px;
  }




</style>