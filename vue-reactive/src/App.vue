<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="page">
    <div class="flex bg-slate-800 h-[4vw] items-center">
      <RouterLink class="text-[2vw] text-sky-500 px-[3vw] font-serif underline" to="/">Home</RouterLink>
      <RouterLink class="text-[2vw] text-sky-500 px-[3vw] font-serif underline" to="/profile">Profile</RouterLink>
    </div>

    <RouterView/>
  </div>
</template>



<style lang="css" scoped>
.page{
  background-color: rgb(40, 62, 87);
  width: 100vw;
  height: 100vh;
}
</style>
