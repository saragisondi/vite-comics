
<script>
/***********************IMPORT**************/
export default {
  data(){
    return{
    }
  }
}
</script>




<!-- HTML -->
<template>
  <main>
    <div class="jumbotron">
      <!-- <img src="../assets/img/jumbotron.jpg" alt=""> -->
    </div>
  </main>
</template>
<!-- HTML / -->




<!-- SCSS -->
<style lang="scss" scoped>
// USE
  @use '../scss/colors.scss' as *;
  @use '../scss/mixin.scss' as *;

  main{
    background-color:$primary-color ;
    color:$secondary-color;

    .jumbotron{
      background-image: url('../assets/img/jumbotron.jpg');
      @include background-img;
      width: 100%;
      height:500px;

    }
  }
</style>