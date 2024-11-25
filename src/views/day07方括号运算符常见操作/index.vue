<template>
    <div>

    </div>
</template>

<script setup lang="ts">
/**获取值 的类型 */
type User = {
    readonly id:number,
    name: string,
    tel: string,
    address?:string
}
type ValueType = User[keyof User]
// 泛型
type MyReadOnly<T> = {
    +readonly [key in keyof T]: T[key]
}

/**数组一样可以处理 */
const arr = ['admin', 'user', 'client']
type ArrTYpe =typeof arr[number]

/**将数组通过as const转为元组类型后，得到的是具体的字面量类型的联合 */
const arrUqine = ['admin', 'user', 'client'] as const;
type UqineType = typeof arrUqine[number]

const students = [
    {name: '1', age: 2, is: true},
    {name: '2', age: 3, is: false}
]
type StudentType = typeof students[number]
type Res = StudentType[keyof StudentType]

</script>

<style scoped>

</style>