<template>
  <div></div>
</template>

<script setup lang="ts">
interface props {
  count: number
  title: string
}

withDefaults(
  defineProps<//   {
  //     count: number
  //     title: string
  //   }
  props>(),
  {
    count: 0
    // title: ''
  }
)
</script>

<style scoped></style>
