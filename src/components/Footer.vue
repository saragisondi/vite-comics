
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
        <li class="h-150" v-for="(link, index) in footerTop" :key="index">
          <a href="#">
            <img src="{{footerTop[index].img}}">
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

        li{
          margin: 0 20px;
          @include d-flex;
          
          span{
            text-transform:uppercase;
            color: $secondary-color;
            margin: 0 10px;
          }
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