<template>
  <div>
    <h2>测试</h2>
    <p>{{ title }}</p>
  </div>
</template>

<script setup lang="ts">
defineProps({
  title: {
    type: String,
    default: '1223'
  }
})
</script>

<style scoped></style>
