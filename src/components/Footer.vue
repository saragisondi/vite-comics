
<script>
import {footerTop} from '../data/menu'
import{footerMiddle} from'../data/menu'
export default {
  data(){
    return{
      footerTop,
      footerMiddle,
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
            <img :src="link.img">
            <span>{{link.text}}</span>
          </a>
        </li>
      </ul>
    </div>

    <div class="footer-middle">

      <div class="left">
        <div class="container-list" v-for="(link, index) in footerMiddle" :key="index">
          <h2>{{ link.title}}</h2>
          <ul>
            <li v-for="(element, index) in link.links" :key="index">
              <a href="#">{{element}}</a>
            </li>
          </ul>
        </div>
      </div>

      <div class="right">
        <img src="../assets/img/dc-logo-bg.png" alt="logo">
      </div>

    </div>

    <div class="footer-bottom h-100">
      <button>SIGN-UP NOW!</button>
      <div class="social">
        <h2>FOLLOW US</h2>
        <img src="" alt="social">
      </div>
    </div>

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

        li:nth-child(4) img{
          width: 15%;
        }

        li:last-child img{
          width: 40%;
        }

        li{
          @include d-flex;

          img{
            width:20%;
          }
          
          span{
            text-transform:uppercase;
            color: $secondary-color;
            margin: 0 5px;
          }
          
        }

      }
    
    }
    .footer-middle{
      background-image: url('../assets/img/footer-bg.jpg');
      background-repeat: no-repeat;
      background-size: cover;
      @include d-flex;  

      .left{
        display: flex;
        flex-wrap: wrap;

        .container-list{
          width: calc(100% / 3);
        }

        h2{
          color:$secondary-color;
        }

        ul{
          margin-top: 12px;
          
          li{
            margin: 6px 0;
  
            a{
              color:$quaternary-color;
            }
          }
        }
      }
    
    }

    .footer-bottom{
      background-color:#303030;
      @include d-flex;

      .social{
        @include d-flex;
      
        img{
          margin: 0 10px;
        }
      }
    }

  }
</style>