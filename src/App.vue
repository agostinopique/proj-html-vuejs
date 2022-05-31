<template>
  <div>
    <HeaderComp />
    <MainComp />
    <FooterComp />
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue';
import MainComp from './components/MainComp.vue';
import FooterComp from './components/FooterComp.vue';

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp,
    FooterComp
  }
}
</script>

<style lang="scss">
@import './assets/style/general';
@import '@fontsource/lato/400.css';

#hover-btn:hover {
  background-color: #E9570C;
}
#light-hover:hover{
  background-color: #E9570C;
  color: white;
}
#transparent-hover:hover{
  background-color: rgba($color: #000000, $alpha: 0);
  border:  1px solid white;
  color: white;
}

#image-overlay:hover{
  background: rgb(248,95,17);
  background: linear-gradient(0deg, rgba(248,95,17,1) 26%, rgba(255,255,255,1) 100%);
}
</style>

