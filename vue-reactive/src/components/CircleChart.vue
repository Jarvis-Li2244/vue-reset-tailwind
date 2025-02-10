<template>
    <div class="circle bg-sky-100 rounded-[50%] w-[40vw] h-[40vw] m-6 flex justify-evenly items-center flex-wrap">
        <button class="spin-button hover:cursor-pointer bg-linear-65 from-purple-700 via-pink-400 to-orange-300 border-18 border-sky-100 rounded-[50%] w-[14vw] h-[14vw] absolute"><img class="spinner object-fill" src="../images/spinning.png" alt="CircleCenter"></button>
        <CircleSection></CircleSection>
    </div>
</template>

<script setup>
import CircleSection from './CircleSection.vue';

</script>

<style lang="css" scoped>


.spinner{
  animation: 20s linear infinite spin;
}

.circle{
  transition: 2s ease 1 forwards turn;
}

@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}

@keyframes turn {
  to {
    transform: rotate(90deg);
  }
}

</style>