
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
  <div>
    <img src="../assets/img/dc-logo.png" alt="logo">
  </div>
  <ul>
    <li v-for="(link, index) in headerMenu" :key="index">
      <a href="#">{{link.text}}</a>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
  @use '../scss/colors.scss' as *;

  a{
    color:$primary-color;
  }


</style>