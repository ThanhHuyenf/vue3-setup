<template>
  <main>
    <h1>Todolist</h1>
    <p>Here is the todolist page.</p>
    {{ msg }}
    <!-- <div class="flex">
      <button @click="decrease">-</button>
      <span class="mx-4">{{ number }}</span>
      <button @click="increate">+</button>
    </div> -->
    <Item :number="number" @decrese="decrease" @increase="increate" />
  </main>
</template>
<script setup lang="ts">
import { ref } from 'vue'
import Item from '@/components/todolist/item.vue'

const msg = 'Hello Vue 3 + Vite'
const number = ref(1)
const increate = () => {
  number.value++
}

const decrease = () => {
  number.value--
}
</script>
<style scoped>
button {
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 4px;
  padding: 4px 10px;
  cursor: pointer;
  outline: none;
}
</style>
```
