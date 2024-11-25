<template>
    <div>

    </div>
</template>

<script setup lang="ts">
type MyPick<T, U extends keyof T> ={
    [key in U]:T[key]
}

type User = {
    name: string,
    age: number,
    tel?:string
}
type OneUser = MyPick<User, 'name'| 'age'>
</script>

<style scoped>

</style>