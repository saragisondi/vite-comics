
<script>
import {footerTop} from '../data/menu'
export default {
  data(){
    return{
      footerTop,
    }
  }
}
</script>

<template>
  <footer>
    <div class="footer-top">
      <ul>
        <li>
          <a href="#"></a>
        </li>
      </ul>
    </div>

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