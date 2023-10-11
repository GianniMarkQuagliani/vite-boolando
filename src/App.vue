<script>
import Header from './components/Header.vue';
import MainSection from './components/MainSection.vue';
import Footer from './components/Footer.vue';
import Card from './components/Card.vue';

export default {
  nome: 'App',
  components: {
    Header,
    MainSection,
    Footer,
    Card
  },

}
</script>

<template>
  <Header />
  <MainSection />
  <Footer />
</template>

<style lang="scss">

@use './scss/main.scss' as *;

</style>