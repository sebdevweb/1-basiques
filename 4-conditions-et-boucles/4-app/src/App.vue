<script setup>
import { ref } from 'vue'

const list = ref([1, 2, 3])
const show = ref(true)
</script>

<template>
  <button @click="show = !show">AFFICHER / CACHER LA LISTE</button>
  <button @click="list.push(list.length + 1)">AJOUTER UN ITEM A LA FIN DE LA LISTE</button>
  <button @click="list.pop()">RETIRER UN ITEM A LA FIN DE LA LISTE</button>
  <button @click="list.reverse()">INVERSER LA LISTE</button>
  <ul v-if="show && list.length">
    <li v-for="item of list">{{ item }}</li>
  </ul>
  <p v-else-if="list.length">La liste n'est pas vide mais cachée.</p>
  <p v-else>La liste est vide.</p>
</template>

<style scoped>

</style>
