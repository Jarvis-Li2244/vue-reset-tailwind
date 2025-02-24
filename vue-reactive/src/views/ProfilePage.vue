<template>
    <div class="w-full h-[90vh] flex">
        <div class="w-1/3 h-[90vh] flex flex-wrap items-center justify-center text-emerald-600 text-semibold font-serif">
            <button @click=resetProfile() class="card hover:cursor-pointer w-3/5 h-1/9 items-center rounded-xl p-2 text-[2vw] underline">Reset Profile</button>
            <button @click=saveProfile() class="card hover:cursor-pointer w-3/5 h-1/9 items-center rounded-xl p-2 text-[2vw] underline">Save Profile</button>
            <button @click=loadProfile() class="card hover:cursor-pointer w-3/5 h-1/9 items-center rounded-xl p-2 text-[2vw] underline">Load Profile</button>
        </div>
        <div class="w-2/3 h-[90vh] flex justify-center items-center">
            <div class="card w-5/6 h-5/6 flex items-center rounded-xl p-2">
                <div class="w-1/2 h-full flex flex-col items-left justify-center font-serif p-4 text-emerald-600 text-semibold">
                    <h1 class="text-[1.5vw] underline">Name:</h1>
                    <input class="bg-sky-100 w-full h-1/10 text-emerald-600 p-2 rounded-xl m-2" type="text" v-model="name" placeholder="Your Name...">
                </div>
                <div class="w-1/2 h-full flex justify-center items-center">
                    <ProfileCard 
                        v-for="card in profileCard" 
                        :label=profileCard[0].label
                        :info=profileCard[0].info
                        :link=profileCard[0].link
                        :image=profileCard[0].image
                        :title=profileCard[0].title />
                </div>
            </div>
        </div>   
    </div>
</template>

<script setup>
import ProfileCard from '../components/ProfileCard.vue';
import { ref } from "vue";
import { cardList, profileKey, profileCard } from "../components/manyLists.js";

for (let i = 0; i < cardList.length; i++) {
    if (cardList[i].label == profileKey.value) {
        profileCard.value = [cardList[i]]
    }
}

const name = ref('')

let savedCard = [
    {
        slot: 1,
        profCard: [],
        name: '', 
    }
]

function saveProfile() {
    savedCard[0].profCard = profileCard.value
    savedCard[0].name = name.value
    console.log(savedCard)
}

function resetProfile() {
    profileCard.value = [{ 
        title: 'Type', 
        label: "Nickname", 
        image: 'emptyImage.png', 
        type: "", 
        info: "This card serves as a placeholder until you choose a personality card fit for you!",
        link: ""
}]
}
</script>

<style lang="css" scoped>
.card{
  background-color: rgba(64, 198, 198, 0.442);
}
</style>