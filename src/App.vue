<script setup>
import { reactive } from 'vue';
import Person from './components/Person.vue'
const person = reactive({
  name : 'arif',
  age : 33,
  country : 'Bangladesh'
})
</script>

<template>
  {{person.name}} {{ person.age }} {{ person.country }}
  <Person :person="person"/>
</template>

<style scoped>
</style>
