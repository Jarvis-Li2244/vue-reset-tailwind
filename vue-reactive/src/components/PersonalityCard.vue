<template>
    <div class="">
        <h1>{{title}}, {{label}}, {{image}}</h1>
    </div>
</template>

<script setup>
import {sectCirc} from "./CircleChart.vue"

defineProps({
    title: String,
    label: String,
    image: String,
})

console.log(sectCirc[1])
</script>

<style lang="css" scoped>

</style>