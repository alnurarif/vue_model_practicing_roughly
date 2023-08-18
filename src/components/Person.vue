<script setup>
import SingleItem from './SingleItem.vue';
    defineProps(['person'])
</script>

<template>
    <SingleItem v-model="person.name" />
    <SingleItem v-model="person.age" />
    <SingleItem v-model="person.country" /><br/>

    <input type="text" v-model="person.name"><br/>
    <input type="text" v-model="person.age"><br/>
    <input type="text" v-model="person.country"><br/>
</template>

