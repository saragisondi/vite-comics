
<script>
/***********************IMPORT**************/
// importo file card e json
import Cards from '../components/Cards.vue'
import DcComics from '../data/dc-comics.json'

export default {
  name:'Main',
  data(){
    return{
      DcComics,
    }
  },
  components:{
    Cards,
  }
}
</script>




<!-- HTML -->
<template>


  <main>

    <div class="container">

    </div>
    <div class="jumbotron"></div>

    <div class="container-cards">
<!-- 
      <span>CURRENT SERIES</span> -->
      
      
      
      <!-- <button>LOAD MORE</button> -->
      <!-- img
        nomeprodotto -->
        
        <Cards 
        
        />
        
    </div>

  </main>

</template>
<!-- HTML / -->




<!-- SCSS -->
<style lang="scss" scoped>
// USE
  @use '../scss/colors.scss' as *;
  @use '../scss/mixin.scss' as *;
  @use '../scss/utilities.scss' as *;

  main{
    background-color:$primary-color ;
    color:$secondary-color;


    .jumbotron{
      background-image: url('../assets/img/jumbotron.jpg');
      @include background-img;
      width: 100%;
      height:330px;
    }

    .container-cards{
      width: 70%;
      height:500px;
      margin:0 auto;
      @include d-flex;
      justify-content: space-between;
      flex-wrap: wrap;

      span{
        background-color: $tertiary-color;
        padding: 5px 15px;
        margin-bottom:20px
      }
    }
  }
</style>