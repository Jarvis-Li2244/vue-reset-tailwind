<template>
    <RouterLink :class= color,orientation class="circleSection w-1/2 h-1/2 border-sky-100" :to=link></RouterLink>
</template>

<script setup>
defineProps({
    color: String,
    orientation: String,
    link: String
})
</script>

<style lang="css" scoped>

</style>