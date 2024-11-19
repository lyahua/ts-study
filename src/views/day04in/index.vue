<template>
    <div>

    </div>
</template>

<script setup lang="ts">
type U = 'a' | 'b' |'c';
type Foo =  {
    [key in U] : string
}

type User = {
    readonly id: number,
    name: string,
    tel: string;
    address?: string
}
type CopyUser = {
    [key in keyof User]: User[key]
}

// 增加泛型
type MyCopy<T> = {
    [key in keyof T]: T[key]
}

type ACopyt = MyCopy<User>
const A:ACopyt = {
    id: 123,
    name: '123',
    tel: '123'
}

</script>

<style scoped>

</style>