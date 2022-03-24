<template>
  <div id="app">
    <MyHeader/>
    <MyMain/>
    <MyFooter/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import MyFooter from './components/MyFooter.vue'


export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter
  }
}
</script>

<style lang="scss">
@import '@fortawesome/fontawesome-free/css/all.css';
@import './assets/scss/common.scss';
@import './assets/scss/layout.scss';
@import './assets/scss/mixin.scss';
@import './assets/scss/mediaquery.scss';


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  flex-direction: column;
}
</style>
