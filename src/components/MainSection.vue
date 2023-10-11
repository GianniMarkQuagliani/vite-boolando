<script>
import prodotti from '../data/prodotti';

export default {
  name: 'MainSection',
  data() {
    return {
      prodotti: prodotti,
    };
  },
};
</script>


<template>
<main>
  <section>
    <div class="container row">
      <div class="col" v-for="(prodotto, index) in prodotti" :key="index">
        <div class="box">
          <img class="image1" :src="prodotto.primaryImage" :alt="prodotto.marca">
          <img class="image2" :src="prodotto.secondaryImage" :alt="prodotto.marca">
          <div class="discount">{{ prodotto.discount }}</div>
          <div class="box-sostenibilità" v-if="prodotto.sostenibilita">Sostenibilità</div>
          <div class="hearts">&hearts;</div>
        </div>
        <div class="img-txt">
          <p>{{ prodotto.marca }}</p>
          <h4>{{ prodotto.modello }}</h4>
          <strong v-if="prodotto.fullPrice">{{ prodotto.fullPrice.toFixed(2) }} &euro;</strong>
          <span>{{ prodotto.lastPrice.toFixed(2) }} &euro;</span>
        </div>
      </div>
    </div>
  </section>
</main>
</template>