<script>
// Importa il componente Header
import Header from './components/Header.vue';

// Importa il componente MainSection
import MainSection from './components/MainSection.vue';

// Importa il componente Footer
import Footer from './components/Footer.vue';

// Importa il componente Card
import Card from './components/Card.vue';

export default {
  // Nome del componente principale
  nome: 'App',
  components: {
    // Registra il componente Header all'interno di App
    Header,
    // Registra il componente MainSection all'interno di App
    MainSection,
    // Registra il componente Footer all'interno di App
    Footer,
    // Registra il componente Card all'interno di App
    Card
  },

}
</script>

<template>

  <!-- Rappresenta la struttura del componente principale -->
  <Header /> <!-- Include il componente Header -->
  <MainSection /> <!-- Include il componente MainSection -->
  <Footer /> <!-- Include il componente Footer -->

</template>

<style lang="scss">

// Importa gli stili SCSS
@use './scss/main.scss' as *;

</style>