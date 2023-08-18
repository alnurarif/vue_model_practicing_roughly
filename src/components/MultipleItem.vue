
<script setup>
defineProps(['name','age','country'])
defineEmits(['update:name','update:age','update:country'])
</script>

<template>
    <div>
        <input type="text" :value="name" @input="$emit('update:name',$event.target.value)">
        <input type="text" :value="age" @input="$emit('update:age',$event.target.value)">
        <input type="text" :value="country" @input="$emit('update:country',$event.target.value)">
    </div>
</template>

