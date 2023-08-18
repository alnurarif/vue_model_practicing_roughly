<script setup>
    defineProps(['person'])
</script>

<template>
    <input type="text" v-model="person.name">
    <input type="text" v-model="person.age">
    <input type="text" v-model="person.country">
</template>

