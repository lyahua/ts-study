<template>
  <div></div>
</template>

<script setup lang="ts">
// type User = {
//   id: number
//   name: string
//   age: number
// }
// type UserKeys = keyof User & {}

// ----------
// const user = {
//   id: 1,
//   name: 'hayes',
//   age: 19
// }
// type UserKeys = keyof typeof user

type Person = {
  age: number
  name: string
  sex: boolean
}
type A = Person[keyof Person]

// 结合着泛型，方括号运算符以及extends受限的泛型，可以直接重写代码
type TagName = keyof HTMLElementTagNameMap & {}

function createElement<T extends TagName>(tag: T): HTMLElementTagNameMap[T] {
  return document.createElement(tag)
}
</script>

<style scoped></style>
