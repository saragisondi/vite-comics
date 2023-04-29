
<script>

import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Cards from './components/Cards.vue'

export default {
  data(){
    return{
    }
  },
  components:{
    Header,
    Main,
    Footer,
    Cards
  }
}
</script>

<template>

  <Header />
  <Main />
  <Footer />
  <Cards />
  
</template>

<style lang="scss">
@use './scss/general.scss' ;
@use './scss/colors.scss';
@use './scss/utilities.scss'
</style>