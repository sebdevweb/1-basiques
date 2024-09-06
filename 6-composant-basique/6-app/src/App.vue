<script setup>
  import { ref } from 'vue'
  import TodoItem from './TodoItem.vue'

  const groceryList = ref([
    {
      id: 0,
      text: 'Légumes'
    }, {
      id: 1,
      text: 'Fromage'
    }, {
      id: 2,
      text: 'Toute autre chose comestible pour les humains'
    }
  ])
</script>

<template>
  <ol>
    <TodoItem 
      v-for="item in groceryList"
      :todo = "item"
      :key = "item.id"
    />
  </ol>
</template>

<style scoped>

</style>
