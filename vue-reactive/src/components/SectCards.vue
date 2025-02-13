
<template>
    <PersonalityCard v-for="card in cards" :key="title" :card="card"/>
</template>

<script setup>
import { reactive, onMounted } from 'vue';
import { useRoute } from 'vue-router';
import PersonalityCard from './PersonalityCard.vue';

const route = useRoute()
const cards = reactive([]);

const cardList = [
    { title: 'ISFJ-NTXLOIDKWHATIMDOINGYEAHKDS', name:"The Placheolder", type: "analysts",  image: 'sometype of url/link coming from images folder' },
    { name: "analysts", title: 'Card 2', description: 'This is card number 2' },
    { name: "analysts", title: 'Card 3', description: 'This is card number 3' },
    { name: "analysts", title: 'Card 4', description: 'This is card number 4' },
    { name: "analysts", title: 'Card 5', description: 'This is card number 5' },
    { name: "analysts", title: 'Card 6', description: 'This is card number 6' },
    { name: "analysts", title: 'Card 7', description: 'This is card number 7' },
    { name: "random", title: 'Card 8', description: 'This is card number 8' },
    { name: "analysts", title: 'Card 9', description: 'This is card number 9' },
    { name: "analysts", title: 'Card 10', description: 'This is card number 10' }
];

onMounted(() => {
    const cardName = route.params.name;
    cardList
        .filter(item => item.type === cardName)
        .forEach(item => cards.push(item))
});
</script>

<style scoped>

</style>
  