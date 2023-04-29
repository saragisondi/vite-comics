
<script>
export default {
  name:'Cards',

  props:{
  thumb:String,
  series:String
  }

}
</script>

<template>

    <div class="cards">
      <div class="container-img">
        <img :src="thumb" :alt="series">
      </div>

      <div class="container-title">
        <div>{{series}}</div>
      </div>
    </div>
  

</template>

<style lang="scss" scoped>
@use '../scss/mixin.scss' as *;


      .cards{
        width: calc(90% / 6);
        height:35%;
        margin-top:50px;
        
        .container-img{
          width: 100%;
          height:80%;
          
          
          img{
            width: 100%;
            height:100%;
            object-fit: cover;
            object-position: top;
            
          }
        }

        div{
          font-size: small;
        }
      }
/* word-wrap:break-word */

</style>