<template>
    <div class="bg-sky-100 rounded-[50%] w-[40vw] h-[40vw] m-6 flex justify-evenly items-center flex-wrap">
        <div class="bg-rose-300 border-18 border-sky-100 rounded-[50%] w-[14vw] h-[14vw] absolute"><img class="spinner object-fill" src="../images/spinning.png" alt="CircleCenter"></div>
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

@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}

</style>