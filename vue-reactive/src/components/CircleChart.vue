<template>
  <div class="circle bg-sky-100 rounded-[50%] w-[40vw] h-[40vw] m-6 flex justify-evenly items-center flex-wrap">
      <button @click=colorChange(sectCirc) class="spin-button hover:cursor-pointer bg-linear-65 from-purple-700 via-pink-400 to-orange-300 border-18 border-sky-100 rounded-[50%] w-[14vw] h-[14vw] absolute">
        <img class="spinner object-fill" src="../images/spinning.png" alt="CircleCenter">
      </button>
      <CircleSection
        v-for="sect in sectCirc" 
        :key="sect.name" 
        :color="sect.color" 
        :orientation="sect.orientation"
        :name="sect.name"
      />
  </div>
</template>

<script setup>
import { reactive } from 'vue';
import CircleSection from './CircleSection.vue';

const sectCirc = reactive([
  {
      color: "from-purple-600 to-fuchsia-500",
      orientation: "bg-linear-135 border-t-[1.5vw] border-l-[1.5vw] border-b-[0.5vw] border-r-[0.5vw] rounded-tl-[100%]",
      name: "analysts"
  },
  {
      color: "from-blue-600 to-sky-500",
      orientation: "bg-linear-225 border-t-[1.5vw] border-l-[0.5vw] border-b-[0.5vw] border-r-[1.5vw] rounded-tr-[100%]",
      name: "sentinels"
  },
  {
      color: "from-orange-400 to-yellow-400",
      orientation: "bg-linear-45 border-t-[0.5vw] border-l-[1.5vw] border-b-[1.5vw] border-r-[0.5vw] rounded-bl-[100%]",
      name: "explorers"
  },
  {
      color: "from-green-700 to-emerald-500",
      orientation: "bg-linear-315 border-t-[0.5vw] border-l-[0.5vw] border-b-[1.5vw] border-r-[1.5vw] rounded-br-[100%]",
      name: "diplomats"
  }
])

function colorChange (sectCirc) {
  let firstSect = [sectCirc[0].color, sectCirc[0].name]
  let secondSect = [sectCirc[1].color, sectCirc[1].name]
  let thirdSect = [sectCirc[2].color, sectCirc[2].name]
  let fourthSect = [sectCirc[3].color, sectCirc[3].name]

  sectCirc[0].color = thirdSect[0] 
  sectCirc[0].name = thirdSect[1]

  sectCirc[1].color = firstSect[0] 
  sectCirc[1].name = firstSect[1]

  sectCirc[2].color = fourthSect[0] 
  sectCirc[2].name = fourthSect[1]

  sectCirc[3].color = secondSect[0]
  sectCirc[3].name = secondSect[1]
}

</script>

<style lang="css" scoped>


.spinner{
  animation: 20s linear infinite spin;
}


@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}


</style>