<script setup>
import { ref, reactive } from 'vue';
import Person from './components/Person.vue'
import SingleItem from './components/SingleItem.vue'
import MultipleItem from './components/MultipleItem.vue';
import ButtonItem from './components/ButtonItem.vue';
const person = reactive({
  name : 'arif',
  age : 33,
  country : 'Bangladesh'
})

const namea = ref('')
</script>

<template>
  <p>{{person.name}} {{ person.age }} {{ person.country }}</p>
  <p>ref name : {{ namea }}</p>
  <!-- <Person :person="person"/> -->
  <br/>
  <!-- niche amra :name evabe kore pathaini karon evabe kore pathale SingleItem theke etake defineProps(['name'])
  diye receive korar por input e v-model="name" dile error dekhato. child e change korle parent e change hoto na. mane parent e 
  write able na. tai v-model hisebe pass korte hobe component e. erpor etake normal ekta variable hisebe recv korbo defineProps(['modelValue'])
  evabe. erpor input e <input type="text" :value="modelValue" @input="$emit('update:modelValue', $event.target.value)" /> evabe likhbo. 
  ekhane @input ta hocche event ei event e modelValue ta update hobe target.value diye mane input tar udpated value diye-->
  <!-- <SingleItem v-model="namea"/> -->
  
  <MultipleItem v-model:name="person.name" v-model:age="person.age" v-model:country="person.country" />
  
  <!-- nicher item ti click korar shateh sathe amader pass kora model ti change hoye reverse hoye jabe-->
  <ButtonItem v-model:name="person.name" />
  <ButtonItem v-model:name="person.age" />
  <ButtonItem v-model:name="person.country" />
</template>

<style scoped>
</style>
