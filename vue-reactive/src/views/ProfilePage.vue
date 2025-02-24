<template>
    <div class="w-full h-[90vh] flex">
        <div class="w-1/3 h-[90vh] flex items-center justify-center text-emerald-600 text-semibold font-serif">
            <button @click=resetProfile(card) class="card hover:cursor-pointer w-3/5 h-1/9 items-center rounded-xl p-2 text-[2vw] underline">Reset Profile</button>
            <button @click=saveProfile(card) class="card hover:cursor-pointer w-3/5 h-1/9 items-center rounded-xl p-2 text-[2vw] underline">Save Profile</button>
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
import { ref, reactive } from "vue";
import { cardList, profileKey, profileCard, sectCirc } from "../components/manyLists.js";

for (let i = 0; i < cardList.length; i++) {
    if (cardList[i].label == profileKey.value) {
        profileCard.value = [cardList[i]]
    }
}
console.log(profileCard.value)

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
    savedCard[0].profCard = [profileCard[0]]
    savedCard[0].info = [information[0]]
}

function resetProfile(card) {

}
</script>

<style lang="css" scoped>
.card{
  background-color: rgba(64, 198, 198, 0.442);
}
</style>