<template>
  <div class="home">
    <Header />
    <Hero />
    <Banner />
    <Insta />
    <Partner />
    <Footer />
    
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue';
import Hero from '@/components/Hero.vue';
import Banner from '@/components/Banner.vue';
import Insta from '@/components/Insta.vue';
import Partner from '@/components/Partner.vue'; 
import Footer from '@/components/Footer.vue';

export default {
  name: 'Home',
  components: {
    Header,
    Hero,
    Banner,
    Insta,
    Partner,
    Footer
  }
}
</script>
