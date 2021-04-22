<template>
  <div>
    <Header />
    <Slide />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Slide from '@/components/Slide.vue'
import Main from '@/components/Main.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    Header,
    Slide,
    Main,
    Footer
  }
 
}
</script>
