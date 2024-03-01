<template>
  <HeaderComponent />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import HeaderComponent from './components/HeaderComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent
  }
}
</script>

<style>
html,body{
  background-image: url('./assets/images/background_light.png');
  margin: 0;
  background-color: #F13737;
}
#app {
  max-width: 100vw;
  overflow: hidden;
}
* {
  -webkit-touch-callout: none; /*系统默认菜单被禁用*/
  -webkit-user-select: none; /*webkit浏览器*/
  -khtml-user-select: none; /*早期浏览器*/
  -moz-user-select: none; /*火狐*/
  -ms-user-select: none; /*IE10*/
  user-select: none;
  color: #fff;
}
:root {
  --van-swipe-indicator-active-background-color: #fff;
  --van-swipe-indicator-inactive-background-color: #bababa;
  --van-swipe-indicator-size: 8px;
}
.rtl_p {
  direction: rtl;
}
</style>
