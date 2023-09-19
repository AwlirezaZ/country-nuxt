<template>
    <div>
        <label v-if="label" :for="id">{{ label }}</label>
        <input v-if="childValue" :name="name" :id="id" :v-model="childValue" :type="type">
    </div>
</template>
<script setup>
import {string} from 'vue-types'
const props = defineProps({
    id: string(),
    name: string(),
    label: string(),
    type: string().def('text'),
    modelValue: string().req,

})
const childValue= modelValue.value
</script>