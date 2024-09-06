<script setup>
  import { ref } from 'vue'

  const text = ref('Edite-moi')
  const checked = ref(true)
  const checkedNames = ref(['jean'])
  const picked = ref('Un')
  const selected = ref('A')
  const multiSelect = ref(['A'])

</script>

<template>

  <fieldset>
    <h2>Champ de texte</h2>
    <input type="text" v-model="text">
    <p>{{ text }}</p>
  </fieldset>

  <fieldset>
    <h2>Case à cocher</h2>
    <input type="checkbox" id="checkbox" v-model="checked">
    <label for="checkbox">Cochée : {{ checked }}</label>
  </fieldset>

  <fieldset>
    <h2>Cases à cocher multiples</h2>
    <input type="checkbox" id="jean" value="jean" v-model="checkedNames">
    <label for="jean">Jean</label>
    
    <input type="checkbox" id="michel" value="michel" v-model="checkedNames">
    <label for="michel">Michel</label>
    
    <input type="checkbox" id="brigitte" value="brigitte" v-model="checkedNames">
    <label for="brigitte">Brigitte</label>

    <p>Nom(s) coché(s) : {{ checkedNames }}</p>
  </fieldset>

  <fieldset>
    <h2>Radio</h2>
    <input type="radio" id="un" value="Un" v-model="picked">
    <label for="un">Un</label>
    <br>
    <input type="radio" id="deux" value="Deux" v-model="picked">
    <label for="deux">Deux</label>
    <br>
    <input type="radio" id="trois" value="Trois" v-model="picked">
    <label for="trois">Trois</label>
    <br>
    <p>Choisi : {{ picked }}</p>
  </fieldset>

  <fieldset>
    <h2>Sélection</h2>
    <select v-model="selected">
      <option disabled value="">Sélectionnez-en-un</option>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
    <p>Sélectionné : {{ selected }}</p>
  </fieldset>

  <fieldset>
    <h2>Sélection multiple</h2>
    <select v-model="multiSelect" multiple style="width: 200px">
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
  </fieldset>
  <p>Sélectionné : {{ multiSelect }}</p>
</template>

<style scoped>

</style>
