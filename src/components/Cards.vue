
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
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div>

<!-- 
  <div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div>
  <div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div>
  <div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div>
  <div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div>
  <div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div><div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div>
  <div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div>
  <div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div>
  <div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div>
  <div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div>
  <div class="cards">
    <img :src="thumb" :alt="series">
    <h1>{{ series }}</h1>
  </div> -->


</template>

<style lang="scss" scoped>
@use '../scss/mixin.scss' as *;

.cards{
  border:1px solid white;
  width: calc(90% / 6);
  height:170px;
  @include d-flex;
  margin-top:50px;
}
/* word-wrap:break-word */

</style>