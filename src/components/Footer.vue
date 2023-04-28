
<script>
import {footerTop} from '../data/menu'
import{footerMiddle} from'../data/menu'
import{footerBottom} from '../data/menu'

export default {
  data(){
    return{
      footerTop,
      footerMiddle,
      footerBottom
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

        <div class="row">
          <div class="container-list">
            <div class="col" v-for="(link, index) in footerMiddle" :key="index">
              <h2>{{link.title}}</h2>
              <ul>
                <li v-for="(element, index) in link.links" :key="index">
                  <a href="#">{{element}}</a>
                </li>
              </ul>
              <h2>{{ link.title2 }}</h2>
              <ul>
                <li v-for="(element, index) in link.links2" :key="index">
                  <a href="#">{{ element }}</a>
                </li>
              </ul>
            </div>
          </div>
        </div>

      </div>

      <div class="right">
        <img src="../assets/img/dc-logo-bg.png" alt="logo">
      </div>

    </div>

    <div class="footer-bottom">
      <button>SIGN-UP NOW!</button>
      <div class="social">
        <h2>FOLLOW US</h2>
        <div>
          <ul>
            <li v-for="(img,index) in footerBottom" :key="index">
              <img :src="img.img" alt="social">
            </li>
          </ul>
        </div>
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
      padding: 20px;
      position:relative;
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
      padding:50px;
      display: flex;
      

      .left{
        margin-left:110px;
        .container-list{
          display: flex;
        }
        .col{
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

            a:hover{
              color:white;
            }
          }
        }
      }

      .right{
        
        img{
          position: absolute;
          top:150px;
          right:150px;
        }

      }
    
    }

    .footer-bottom{
      background-color:#303030;
      padding: 20px;
      position:relative;
      @include d-flex;

      button{
        border: 2px solid $tertiary-color;
        background-color: $quinary-color;
        color: $secondary-color;
        padding:10px;
      }
      .social{
        @include d-flex;
      
        ul{
          @include d-flex;
          margin:0 20px;
        }

        h2{
          color:$tertiary-color;
          font-size:medium;
          font-weight:bold;
        }
        img{
          margin: 0 10px;
          width: 30px;
        }
      }
    }

  }
</style>