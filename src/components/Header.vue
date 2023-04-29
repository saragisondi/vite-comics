
<script>
/*******************IMPORT***************/
import{headerMenu} from '../data/menu'

export default {
  name:'Header',
  data(){
    return{
      headerMenu,
      counter: 0,
    }
  },
  
}
</script>




<!--HTML -->
<template>
  <header>
    <!--LOGO -->
    <div class="container-img">
      <img src="../assets/img/dc-logo.png" alt="logo">
    </div>
  
    <!-- NAVBAR -->
    <nav>
      <ul>
        <li v-for="(link, index) in headerMenu" :key="index">
          <a @click="counter = index" :class="{'active' : counter == index}" href="#">{{link.text}}</a>
        </li>
      </ul>
    </nav>

  </header>

</template>
<!--HTML /-->


<!--SCSS -->
<style lang="scss" scoped>
// USE
  @use '../scss/general.scss' as *;
  @use '../scss/colors.scss' as *;
  @use '../scss/mixin.scss' as *;
  
  
  header{
    @include space-around;
    padding:10px;
    .container-img{
      width: 70px;
    }
    ul{
      @include d-flex;

      
      li{
        margin:0 10px;
        text-transform:uppercase;
        font-weight: bold;
        font-size:smaller;

        a:hover{
            color: $tertiary-color;
            border-bottom: 3px solid $tertiary-color;
          }
        
        a{
          color:$primary-color;
          padding-bottom:30px;
        }
      }
    }
      
    
  }


</style>