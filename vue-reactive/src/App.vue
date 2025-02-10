<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="page">
    <div class="header flex h-[10vh] items-center">
      <RouterLink class="text-[2vw] text-emerald-600 rounded-lg bg-white mx-[2vw] px-[4vw] font-serif font-semibold underline" to="/">Home</RouterLink>
      <RouterLink class="text-[2vw] text-emerald-600 rounded-lg bg-white mx-[2vw] px-[4vw] font-serif font-semibold underline" to="/profile">Profile</RouterLink>
    </div>
    <div class="interactive flex h-[90vh] justify-evenly items-center">
      <RouterView/>
      <div class="infobox w-[28vw] h-5/6 bg-teal-100 rounded-xl border-6">
        <h1 class="text"></h1>
      </div>
    </div>
  </div>
</template>



<style lang="css" scoped>
.page{
  background-color: rgb(255, 255, 255);
  width: 100vw;
  height: 100vh;
}
.header{
  background-color: rgb(0, 146, 146);
}
.infobox{
  border-color: rgb(0, 146, 146);
  overflow-y: scroll;
}
.text{
  font-size: 32;
}
</style>
