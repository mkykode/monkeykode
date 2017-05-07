<template>
  <div id="app">
    <vue-particles class="particles" color="#dedede"></vue-particles>
    <app-header></app-header>
    <div class="container">
      <app-content></app-content>
    </div>
    <app-footer></app-footer>
  </div>
</template>

<script>
  import Header from './components/Header.vue'
  import Content from './components/Content.vue'
  import Footer from './components/Footer.vue'
  export default {
    name: 'app',
    components: {
      'app-header': Header,
      'app-content': Content,
      'app-footer': Footer
    }
  }
</script>

<style lang="scss">
  #app {

    .particles {
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      z-index: -100;
    }
  }


</style>
