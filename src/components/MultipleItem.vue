
<script setup>
defineProps(['name','age','country'])
const emit = defineEmits(['update:name','update:age','update:country'])
const updateCountry = (value) => {
    emit('update:country', value)
}
</script>

<template>
    <div>
        <input type="text" :value="name" @input="$emit('update:name',$event.target.value)">
        <input type="text" :value="age" @input="$emit('update:age',$event.target.value)">
        <input type="text" :value="country" @input="updateCountry($event.target.value)">
    </div>
</template>

