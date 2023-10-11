<script>
// Importa i dati dei prodotti da prodotti.js
import prodotti from '../data/prodotti';

// Importa il componente Card
import Card from './Card.vue';

export default {
  // Nome del componente
  name: 'MainSection',

  // Inizializza la variabile prodotti con i dati importati
  data() {
    return {
      prodotti: prodotti,
    };
  },

  // Registra il componente Card all'interno di MainSection
  components: {
    Card, // Registra il componente Card all'interno di MainSection
  },
};
</script>

<template>
  <main>
    <section>
      <div class="container row">
        <!-- Itera attraverso la lista di prodotti e crea un componente Card per ciascun prodotto -->
        <card
          v-for="(prodotto, index) in prodotti"
          :key="index"
          :prodotto="prodotto" 
        /> <!-- Passa il prodotto come prop al componente Card -->
      </div>
    </section>
  </main>
</template>
