<script>
  export default {
    
  }
</script>

<template>
  <div class="community container-fluid d-flex justify-content-center align-items-center flex-column text-center text-white">
    <div class="my_container">
    <h2 class="fw-bold">Hey! Join to our <br> Community</h2>
    <p class="m-5">Nulla molestie tortor nec lectus venenatis, sed blandit dui finibus. Curabitur feugiat vuluptate purus ipsums dolores ficilis uns etra.</p>
    <button type="button" class="my_btn my-4 text-white">SIGN UP &nbsp;></button>
  </div>
  </div>
</template>


<style lang="scss" scoped>
@use '/src/assets/scss/partials/variables' as *;

.community{
  background-image: url(/public/img/join_now_cta_bg.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  .my_container{
    width: 800px;
    padding: 80px;
    p{
      font-size: 14px;
    }
    h2{
      font-size: 45px;
    }
  }
 .my_btn{
  background-color: $easternblue;
      padding: 7px 30px;
      border: none;
      &:hover{
        background-color: #f0926b;
        transition: all .3s ease-out;
      }
    }
}

</style>