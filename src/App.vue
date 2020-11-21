<template>
  <div class="fl w-100 vh-100 flex flex-column" id="app">
    <Header/>
    <router-view class="h-100" />
    <Footer/>
  </div>
</template>

<script>
import Header from '@/components/Header'
import Footer from '@/components/Footer'
export default {
  name: 'App',
  components: { Header, Footer }
}
</script>

<style media="screen">
    @import 'assets/css/tachyons.css';
    @import 'assets/css/fontawesomepro.css';
    @import 'assets/css/style.css';
    
</style>
