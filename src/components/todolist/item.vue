<template>
  <div class="flex">
    <button @click="$emit('decrese')">-</button>
    <span class="mx-4">{{ number }}</span>
    <button @click="$emit('increase')">+</button>
  </div>
</template>
<script setup lang="ts">
const props = defineProps(['number'])
</script>
