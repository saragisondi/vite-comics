
<script>
import{headerMenu} from '../data/menu'

export default {
  
  data(){
    return{
      headerMenu,
    }
  }
}
</script>

<template>

  <header>
    <div class="container-img">
      <img src="../assets/img/dc-logo.png" alt="logo">
    </div>
  
    <ul>
      <li v-for="(link, index) in headerMenu" :key="index">
        <a href="#">{{link.text}}</a>
      </li>
    </ul>
  </header>

</template>

<style lang="scss" scoped>
  @use '../scss/general.scss' as *;
  @use '../scss/colors.scss' as *;
  @use '../scss/font.scss' as *;

  
  header{
    @include d-flex;
    ul{
      display:flex;

      li{
        margin:0 10px;
        text-transform:uppercase;
        font-weight: bold;

        a{
          color:$primary-color;
        }
      }
    }
      
    
  }


</style>