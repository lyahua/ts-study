<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import CountView from './views/CountView.vue'
import { ref } from 'vue'

const refCountView = ref<InstanceType<typeof CountView> | null>(null)
const title = ref<string>('1111')

interface Item {
  id: string
  name: string
  age?: number
}
interface ReturnResult<T> {
  code: number
  message: string
  data: T[]
}

function identity<T>(arg: T): T {
  return arg
}

async function getData(): Promise<string> {
  return await ''
}
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />

  <hr />
  <CountView :title="title" />
</template>

<style scoped></style>
