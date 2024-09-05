<script setup>
  import { ref } from 'vue'

  const message = ref('Hell SFC Vue!')

  function reverseMessage() {
    message.value = message.value.split('').reverse().join('')
  }
  function notify() {
    alert('MESSAGE AFFICHER SANS RECHARGER LA PAGE')
  }
</script>

<template>
  <h1>{{ message }}</h1>
  <button @click="reverseMessage">REVERSE MESSAGE</button>
  <button @click="message += '@' ">ADD '@'</button>
  <button @click.prevent="notify">AFFICHER ALERTE</button>
</template>

<style scoped>

</style>
