<script setup>
import { ref } from 'vue'
const showText = ref(false)
const number = ref(2)

const changeText = () => {
  showText.value = !showText.value
  console.log(number.value)
  number.value = 3
}
</script>

<template>
  <!-- stworzenie modala i przycisku otwierajacego moodala  -->
  <!-- na modalu przycisk do zamykania modala -->
  <ul class="nav">
    <li @click="changeText">Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ul>

  <div>{{ number }}</div> <br>
  <div v-if="showText">To jest Kawa!</div>
</template>

<style scoped>
/* ostylowac nawigacje  */
/* 100% szerokosci */
/* usuniecie kropek */
/* wysrodkowanie */
/* ustawienie wielkosci czcionki */
/* co drugi napis czerwony */
/* Pierwszy element w kole zielonym */
.nav {
  display: flex;
  flex-wrap: wrap;
  background-color: blue;
  color: yellow;
}

.nav > li {
  padding: 5px 5px 5px 5px;
  cursor: pointer;
}
</style>
