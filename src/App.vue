<template>
  <div id="app">
<Header/>
<Main/>
<Footer/>
  </div>
</template>

<script>
import Header from './components/Macro/Header.vue'
import Main from './components/Macro/Main.vue'
import Footer from './components/Macro/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import './assets/style/global.scss';

</style>
