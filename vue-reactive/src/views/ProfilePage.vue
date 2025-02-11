<template>
    <div class="circle bg-sky-100 rounded-[50%] w-[40vw] h-[40vw] m-6 flex justify-evenly items-center flex-wrap">
        <button class="spin-button hover:cursor-pointer bg-linear-65 from-purple-700 via-pink-400 to-orange-300 border-18 border-sky-100 rounded-[50%] w-[14vw] h-[14vw] absolute"><img class="spinner object-fill" src="../images/spinning.png" alt="CircleCenter"></button>
        <TestComponent v-for="(sect, index) in circleSects" :key="index" :sect="sect"></TestComponent>
        <li v-for="(sect, index) in circleSects">{{ sect.angle }}</li>
    </div>
</template>

<script setup>
import TestComponent from '../components/TestComponent.vue';


const circleSects = [
    {
        angle: 135, 
        initColor: "purple-600", 
        finalColor: "fuchsia-500", 
        top: "1.5vw", 
        left: "1.5vw", 
        bottom: "0.5vw", 
        right: "0.5vw"
    }, 
    {
        angle: 135, 
        initColor: "purple-600", 
        finalColor: "fuchsia-500", 
        top: "1.5vw", 
        left: "1.5vw", 
        bottom: "0.5vw", 
        right: "0.5vw"
    },
    {
        angle: 135, 
        initColor: "purple-600", 
        finalColor: "fuchsia-500", 
        top: "1.5vw", 
        left: "1.5vw", 
        bottom: "0.5vw", 
        right: "0.5vw"
    },
    {
        angle: 135, 
        initColor: "purple-600", 
        finalColor: "fuchsia-500", 
        top: "1.5vw", 
        left: "1.5vw", 
        bottom: "0.5vw", 
        right: "0.5vw"
    },
]

</script>

<style lang="css" scoped>

</style>