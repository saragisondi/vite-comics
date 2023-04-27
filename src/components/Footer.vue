
<script>
export default {
  
}
</script>

<template>
  <footer>
    <div class="footer-top">list</div>
    <div class="footer-middle">logo</div>
    <div class="footer-bottom">social</div>
  </footer>
</template>

<style lang="scss" scoped>
  @import '../scss/colors.scss';

  footer{

    .footer-top{
      background-color: $tertiary-color;
    }
    .footer-middle{
      background-image: url('../assets/img/footer-bg.jpg');
    }

    .footer-bottom{
      background-color:#303030;
    }

  }
</style>