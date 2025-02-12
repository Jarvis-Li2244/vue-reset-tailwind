<template>
    <div class="card flex flex-col justify-evenly itmes-center">
        <h1 class="personType"></h1>
        <div class="imageholder"><img src="" alt=""></div>
        <h2 class="typeTitle"></h2>
    </div>
</template>

<script setup>
defineProps({
    color: String,
    orientation: String,
})

</script>

<style lang="css" scoped>

</style>