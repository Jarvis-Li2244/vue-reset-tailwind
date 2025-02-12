<template>
    <button @click=cardDisplay(name) :class= color,orientation class="circleSection w-1/2 h-1/2 border-sky-100"></button>
</template>

<script setup>
defineProps({
    color: String,
    orientation: String,
    name: String
})

function cardDisplay(end) {
    console.log(end)
    this.$router.push({ name: card, params: { end: end }})
}

</script>

<style lang="css" scoped>

</style>