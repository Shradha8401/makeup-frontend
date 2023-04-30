<template>
  <HeaderComp />
  <MakeupContainer />
  <FooterComp />
</template>

<script>
import HeaderComp from './components/HeaderComp.vue';
import FooterComp from './components/FooterComp.vue';
import MakeupContainer from './components/MakeupContainer.vue';

export default {
  name: 'App',
  components: {
    HeaderComp,
    FooterComp,
    MakeupContainer
  }
}
</script>

<style>
#app {
 
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: rgb(215, 215, 225);
  
}
</style>
