
<script setup>
import {computed} from 'vue'
const props = defineProps(['name','age','country'])
const emit = defineEmits(['update:name','update:age','update:country'])

const personName = computed({
    get(){
        return props.country
    },
    set(value){
        emit('update:country', value)
    }
})

</script>

<template>
    <div>
        <input type="text" :value="name" @input="$emit('update:name',$event.target.value)">
        <input type="text" :value="age" @input="$emit('update:age',$event.target.value)">
        <input type="text" v-model="personName">
    </div>
</template>

