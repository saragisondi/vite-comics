
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

  header{
    @include d-flex;
  }

  a{
    color:$primary-color;
  }

  li{
    background-color:red
  }

  .container-img{
    background-color:black
  }

</style>