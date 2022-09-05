<template>
  <div id="app">
    <MyHeader />
    <MyMain />
    <MyFooter />
  </div>
</template>

<script>

import MyHeader from './components/header/MyHeader.vue';
import MyMain from './components/main/MyMain.vue';
import MyFooter from './components/footer/MyFooter.vue';

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
  @import '~@fortawesome/fontawesome-free/css/all.css';
  @import './assets/styles/general.scss';
</style>
