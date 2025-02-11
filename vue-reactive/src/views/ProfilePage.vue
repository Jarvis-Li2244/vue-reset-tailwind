<template>
    <div class="circle bg-sky-100 rounded-[50%] w-[40vw] h-[40vw] m-6 flex justify-evenly items-center flex-wrap">
        <button class="spin-button hover:cursor-pointer bg-linear-65 from-purple-700 via-pink-400 to-orange-300 border-18 border-sky-100 rounded-[50%] w-[14vw] h-[14vw] absolute"><img class="spinner object-fill" src="../images/spinning.png" alt="CircleCenter"></button>
        <TestComponent v-for="(sect, index) in sectCirc" :key="index" :color="sect.color" :orientation="sect.orientation"></TestComponent>
    </div>
</template>

<script setup>
import TestComponent from '../components/TestComponent.vue';

const sectCirc = [
    {
        color: "from-purple-600 to-fuchsia-500",
        orientation: "bg-linear-135 border-t-[1.5vw] border-l-[1.5vw] border-b-[0.5vw] border-r-[0.5vw] rounded-tl-[100%]"
    },
    {
        color: "from-blue-600 to-sky-500",
        orientation: "bg-linear-225 border-t-[1.5vw] border-l-[0.5vw] border-b-[0.5vw] border-r-[1.5vw] rounded-tr-[100%]"
    },
    {
        color: "from-orange-400 to-yellow-400",
        orientation: "bg-linear-45 border-t-[0.5vw] border-l-[1.5vw] border-b-[1.5vw] border-r-[0.5vw] rounded-bl-[100%]"
    },
    {
        color: "from-green-700 to-emerald-500",
        orientation: "bg-linear-315 border-t-[0.5vw] border-l-[0.5vw] border-b-[1.5vw] border-r-[1.5vw] rounded-br-[100%]"
    }
]

function colorChange (sectCirc) {
    for(let i = 0; i < sectCirc.length; i++) {
        sectCirc
    }
}

</script>

<style lang="css" scoped>

</style>