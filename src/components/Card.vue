<script>
export default {
    // Nome del componente
    name: 'Card',
    props: {
        // Definisci una prop 'prodotto' di tipo oggetto
        prodotto: Object,
    },
};
</script>

<template>
<div class="col">
    <div class="box">
        <!-- Mostra l'immagine principale del prodotto -->
        <img class="image1" :src="prodotto.primaryImage" :alt="prodotto.marca">
        <!-- Mostra l'immagine secondaria del prodotto -->
        <img class="image2" :src="prodotto.secondaryImage" :alt="prodotto.marca">
        <div class="discount">{{ prodotto.discount }}</div>
        <!-- Mostra "Sostenibilità" se la prop sostenibilita è true -->
        <div class="box-sostenibilità" v-if="prodotto.sostenibilita">Sostenibilità</div>
        <div class="hearts">&hearts;</div>
    </div>
    <div class="img-txt">
        <p>{{ prodotto.marca }}</p>
        <h4>{{ prodotto.modello }}</h4>
        <!-- Mostra il prezzo intero se disponibile -->
        <strong v-if="prodotto.fullPrice">{{ prodotto.fullPrice.toFixed(2) }} &euro;</strong>
        <!-- Mostra il prezzo scontato -->
        <span>{{ prodotto.lastPrice.toFixed(2) }} &euro;</span>
    </div>
</div>
</template>