
<script>
/************IMPORT***********************/
import {footerTop} from '../data/menu'
import{footerMiddle} from'../data/menu'
import{footerBottom} from '../data/menu'


export default {
  name:'Footer',
  data(){
    return{
      footerTop,
      footerMiddle,
      footerBottom
    }
  }
}
</script>




<!-- HTML -->
<template>

  <footer>
    <!-- FOOTER TOP -->
    <div class="footer-top">

      <ul>
        <li v-for="(link, index) in footerTop" :key="index">
          <a href="#">
            <img :src="link.img">
            <span>
              {{link.text}}</span>
          </a>
        </li>
      </ul>

    </div>

    <!-- FOOTER MIDDLE -->
    <div class="footer-middle">

      <!-- left-->
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

              <h2 class="shop">{{ link.title2 }}</h2>
              <ul>
                <li v-for="(element, index) in link.links2" :key="index">
                  <a href="#">{{ element }}</a>
                </li>
              </ul>
            </div>
          </div>
        </div>

      </div>

      <!-- right -->
      <div class="right">
      
        <div class="container-img"> 
          <img src="../assets/img/dc-logo-bg.png" alt="logo">
        </div>
      </div>

    </div>


    <!-- FOOTER BOTTOM -->
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
<!-- HTML / -->




<!-- SCSS -->
<style lang="scss" scoped>
  // import
  @import '../scss/colors.scss';
  @import '../scss/general.scss';
  @import '../scss/mixin.scss';


  footer{
    // FOOTER TOP
    .footer-top{
      background-color: $tertiary-color;
      padding: 30px;
      @include space-around;
      
      ul{
        @include space-around;
        
        li:nth-child(4) img{
          width: 20%;
        }
        
        li:last-child img{
          width: 30%;
        }
        
        li:last-child a{
          width: 180px;
        }

        li{
          @include space-around;
      

          img{
            width:25%;
          }
          
          span{
            text-transform:uppercase;
            color: $secondary-color;
            margin: 0 5px;
            font-size: 12px;
          }
          
        }

      }
    
    }

    // FOOTER MIDDLE
    .footer-middle{
      background-image: url('../assets/img/footer-bg.jpg');
      @include background-img;
      display: flex;
      justify-content: space-evenly;
      
      // left
      .left{
        padding:30px;
        .container-list{
          display: flex;
        }
        .col{
          width: calc(100% / 3);
          font-size:small;
          margin:0 5px;
          
          .shop{
            margin-top:20px;
              }
          }

        h2{
          color:$secondary-color;
          font-size: 15px;
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
      // right
      .right{
        width: 30%;
        height: 350px;


        .container-img{
          width: 100%;
          height: 100%;
        }
          
      }
    
    }

    // FOOTER BOTTOM
    .footer-bottom{
      background-color:#303030;
      padding: 20px;
      position:relative;
      @include space-around;

      button{
        border: 2px solid $tertiary-color;
        background-color: $quinary-color;
        color: $secondary-color;
        padding:10px;
      }
      .social{
        @include space-around;
      
        ul{
          @include space-around;
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