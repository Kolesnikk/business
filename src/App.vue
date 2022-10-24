<template>
  <div id="app">
    <Header/>
    <Banner/>
    <About/>
    <Gallery/>
    <Clients/>
    <Footer/>
  </div>
</template>

<script>
import Header from '@/components/banner/Header.vue'
import Banner from '@/components/banner/Banner.vue'
import About from '@/components/about/About.vue'
import Gallery from '@/components/gallery/Gallery.vue'
import Clients from '@/components/clients/Clients.vue'
import Footer from '@/components/footer/footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    About,
    Gallery,
    Clients,
    Footer
  }
}
</script>

<style lang="scss">
  Header {
    z-index: 10;
  }
</style>
