<template>
  <div>
    <Children :count="count" :title="title" />

    <input type="text" ref="el" />
  </div>
</template>

<script setup lang="ts">
import Children from './Children.vue'

import { onMounted, ref } from 'vue'

const count = ref<number>(0)
const title = ref('')

const el = ref<HTMLInputElement | null>(null)

onMounted(() => {
  el.value?.focus()
})
</script>

<style scoped></style>
