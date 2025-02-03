<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    
    <nav>
      <div class="flex bg-gray-800 mb-2">
        <RouterLink class="text-5xl text-emerald-600 mx-[3vw]" to="/">Home</RouterLink>
        <RouterLink class="text-5xl text-emerald-600 mx-[3vw]" to="/profile">Profile</RouterLink>
      </div>
    </nav>

    <RouterView />
</template>



<style scoped>

</style>
