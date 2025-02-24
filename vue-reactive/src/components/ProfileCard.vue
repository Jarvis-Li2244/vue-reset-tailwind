<template>
    <div :class=color class="card w-[20vw] h-[29vw] bg-linear-65 rounded-xl flex flex-col justify-evenly items-center p-4 text-center font-serif text-sky-100 shadow-xl">
        <h1 class="text-[2vw]">{{ profileCard[0].label }}</h1>
        <div class="w-1/2 h-1/3 bg-white p-2 rounded-lg shadow-xl">
            <a :href=profileCard[0].link><img class="hover:cursor-pointer object-fill" :src="'/src/images/' + profileCard[0].image" :alt=profileCard[0].label></a>
        </div>
        <h2 class="text-[1.5vw]">{{ profileCard[0].title }}</h2>
        <h3 class="text-[1vw]">{{ profileCard[0].info }}</h3>
    </div>
</template>

<script setup>
import { ref } from "vue";
import { cardList, profileKey, profileCard, sectCirc } from "./manyLists.js";

for (let i = 0; i < cardList.length; i++) {
    if (cardList[i].label == profileKey.value) {
        profileCard.push(cardList[i])
        console.log(profileCard)
    }
}

let color = ref('')

for(let i = 0; i < sectCirc.length; i++) {
    if (sectCirc[i].name == profileCard[0].type) {
        color = sectCirc[i].color
    }
}

</script>

<style lang="css" scoped>

</style>