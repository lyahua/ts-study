<template>
    <div>

    </div>
</template>

<script setup lang="ts">
type MyCopy<T> = {
    [key in keyof T]: T[key]
}

// 变成只读属性
type MyReadonly<T> = {
   readonly [key in keyof T]: T[key]
}

// 变成可靠属性
type MyPartial<T> = {
    [key in keyof T]?: T[key]
}



</script>

<style scoped>

</style>