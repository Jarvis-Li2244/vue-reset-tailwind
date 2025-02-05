<template>
    <div class="bg-white rounded-[50%] w-[45vw] h-[45vw] m-6 flex justify-evenly items-center flex-wrap">
        <div class="bg-pink-400 rounded-[50%] w-[15vw] h-[15vw] absolute border-4 border-pink-600"><img class="object-fill" src="../images/spinning.png" alt="CircleCenter"></div>
        <CircleSection></CircleSection>
    </div>
</template>

<script setup>
import CircleSection from './CircleSection.vue';
</script>

<style lang="css" scoped>

</style>