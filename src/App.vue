<template>
  <HeaderComponent />
  <leaderBoardComp />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import leaderBoardComp from './components/leaderBoardComp.vue';
export default {
  name: 'App',
  components: {
    HeaderComponent,
    leaderBoardComp
  }
};
</script>

<style>
html,body{
  background-image: url('./assets/images/background_light.png');
  margin: 0;
  background-color: #F13737 !important;
  height: 100vh;
  position: absolute;
  
}
#app {
  max-width: 100vw;
  overflow: hidden;
}

</style>
