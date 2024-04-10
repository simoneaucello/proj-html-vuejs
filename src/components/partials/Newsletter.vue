<script>
  export default {
    
  }
</script>

<template>
  <div class="container-fluid newsletter d-flex justify-content-center align-items-center text-center flex-column ">
    <h5 class="fw-bold">Subscribe to our Newsletter</h5>
    
    <div class="subscribe mb-3">
      <input type="text" placeholder="Insert your email*" class="p-2" aria-label="Username" aria-describedby="addon-wrapping" size="50">
      <button type="submit" class="my_btn btn-dark my-3">SEND</button>
    </div>

  </div>
</template>


<style lang="scss" scoped>
@use '/src/assets/scss/partials/variables' as *;

.newsletter{
  background-color: #f1f1f1;
  padding: 80px;
  .subscribe{

    .my_btn{
      margin-left: 20px;
      background-color: $shark;
      color: white;
      padding: 8px 75px;
    }
   
  }
}

</style>