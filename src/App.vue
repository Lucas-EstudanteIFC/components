<script setup>
import ExpandBox from './components/ExpandBox.vue';
import Card from './components/Card.vue';
import CardFull from './components/CardFull.vue';
const caixas = [
  { id: 1, title: 'Caixa 1', content: 'Conteúdo 1', quantity: 100 },
  { id: 1, title: 'Caixa 2', quantity: 10000 },
  { id: 1, title: 'Caixa 3', content: 'Conteúdo 3' },
  { id: 1, title: 'Caixa 4', content: 'Conteúdo 4', quantity: -60 },
  { id: 1, title: 'Caixa 5', content: 'Conteúdo 5' }
]
</script>

<template>
  <h1>Compenentes e Slots</h1>
  <hr>
  <h2>Aula de Slots</h2>
  <!-- <card title="Card 1">
    <p>Conteúdo do meu Card 1</p>
  </card>
  <card title="Card 2">
  </card> -->

  <CardFull>
    <p>Meus dados</p>
    <template #header>
      <h1>Header</h1>
    </template>
    <template #footer>
      <p>Footer</p>
    </template>
  </CardFull>
  <hr>
  <h2>Aula de Props</h2>
  <expand-box v-for="caixa in caixas" :key="caixa.id" v-bind='caixa' />
  <!-- <ExpandBox title="Caixa-1" />
  <ExpandBox title="Caixa-2" quantity="50" /> -->
</template>

<style scoped></style>
