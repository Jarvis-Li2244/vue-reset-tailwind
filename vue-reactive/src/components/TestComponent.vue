<template>
    <div class="bg-black w-[45vw]" v-for="(sect) in circleSects"><h1>{{ angle, initColor }}</h1></div>
</template>

<script setup>
circleSects = [{angle: 135, initColor: "purple-600", finalColor: "fuchsia-500", top: "1.5vw", left: "1.5vw", bottom: "0.5vw", right: "0.5vw"}, {angle: 135, initColor: "purple-600", finalColor: "fuchsia-500", top: "1.5vw", left: "1.5vw", bottom: "0.5vw", right: "0.5vw"}]
</script>

<style lang="css" scoped>

</style>