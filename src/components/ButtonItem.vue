<script setup>
const prop = defineProps(['name'])
const emit = defineEmits(['update:name'])

const changeTheValue = () => {
    emit('update:name', prop.name.split('').reverse().join(''))
}
</script>
<template>
    <button @click="changeTheValue()" >Update {{prop.name}} </button>
</template>