<template>
    <div class="w-full h-[90vh] flex">
        <div class="w-1/3 h-[90vh] flex items-center justify-center text-emerald-600 text-semibold font-serif">
            <button @click=saveProfile(card) class="card hover:cursor-pointer w-3/5 h-1/9 items-center rounded-xl p-2 text-[2vw] underline">Save Profile</button>
        </div>
        <div class="w-2/3 h-[90vh] flex justify-center items-center">
            <div class="card w-5/6 h-5/6 flex items-center rounded-xl p-2">
                <div class="w-1/2 h-full flex flex-col items-left justify-center font-serif p-4 text-emerald-600 text-semibold">
                    <h1 class="text-[1.5vw] underline">Name:</h1>
                    <input class="bg-sky-100 w-full h-1/10 text-emerald-600 p-2 rounded-xl m-2" type="text" v-model="name" placeholder="Your Name...">
                </div>
                <div class="w-1/2 h-full flex justify-center items-center">
                    <ProfileCard/>
                </div>
            </div>
        </div>   
    </div>
</template>

<script setup>
import ProfileCard from '../components/ProfileCard.vue';
import { ref, reactive } from "vue";
import { profileCard } from '../components/manyLists.js';

const name = ref('')
const information = [{
    name: name,
}]

const savedCard = reactive([
    {
        slot: 1,
        profCard: [],
        info: [], 
    }
])

function saveProfile(card) {
    savedCard[0].profCard.push(profileCard[0])
    savedCard[0].info.push(information[0])
    console.log(savedCard)
}
</script>

<style lang="css" scoped>
.card{
  background-color: rgba(64, 198, 198, 0.442);
}
</style>