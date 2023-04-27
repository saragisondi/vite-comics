
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
        <li v-for="(link, index) in footerTop" :key="index">
          <a href="#">
            <img :src= link.img>
            <span>{{link.text}}</span>
          </a>
        </li>
      </ul>
    </div>

    <div class="footer-middle">logo</div>

    <div class="footer-bottom">social</div>

  </footer>
</template>

<style lang="scss" scoped>
  @import '../scss/colors.scss';
  @import '../scss/general.scss';

  footer{

    .footer-top{
      background-color: $tertiary-color;
      @include d-flex;
      ul{
        @include d-flex;

        li, span{
          margin: 0 20px;
          color: $secondary-color;
          text-transform:uppercase;
        }
      }
    }
    .footer-middle{
      background-image: url('../assets/img/footer-bg.jpg');
    }

    .footer-bottom{
      background-color:#303030;
    }

  }
</style>