<script setup>
import { ref } from 'vue'

const message = ref('Hello Vue!')
const isRed = ref(true)
const color = ref('green')

function toggleRed() {
  isRed.value = !isRed.value
  console.log('toggleRed/Black');
}

function toggleColor() {
  color.value = color.value === 'green' ? 'blue' : 'green'
  console.log('toggleColor');
  
}
</script>

<template>
  
  <p><span :title="message">Passez votre souris sur moi pendant quelques secondes pour voir mon titre lié de manière dynamique !</span></p>

  <p :class=" {red: isRed} " @click="toggleRed">Ceci devrait être rouge... mais cliquez sur moi pour le changer.</p>

  <p :style=" { color } " @click="toggleColor">Cela doit être vert et alterner entre le vert et le bleu lorsque l'on clique dessus.</p>

</template>

<style scoped>
    .red {
      color: red;
    }
</style>
