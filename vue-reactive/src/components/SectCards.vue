
<template>
    <PersonalityCard 
        v-for="card in cards" 
        :key="card.title" 
        :title="card.title"
        :label="card.label"
        :image="card.image"/>
</template>

<script setup>
import { reactive, onMounted } from 'vue';
import { useRoute } from 'vue-router';
import PersonalityCard from './PersonalityCard.vue';

const route = useRoute()
const cards = reactive([]);

const cardList = [
    { title: 'ISFJ-NTXLOIDKWHATIMDOINGYEAHKDS', label:"The Placheolder", image: 'sometype of url/link coming from images folder', type: "analysts"},
    { label: "analysts", title: 'Card 2', description: 'This is card number 2' },
    { label: "analysts", title: 'Card 3', description: 'This is card number 3' },
    { label: "analysts", title: 'Card 4', description: 'This is card number 4' },
    { label: "analysts", title: 'Card 5', description: 'This is card number 5' },
    { label: "analysts", title: 'Card 6', description: 'This is card number 6' },
    { label: "analysts", title: 'Card 7', description: 'This is card number 7' },
    { label: "random", title: 'Card 8', description: 'This is card number 8' },
    { label: "analysts", title: 'Card 9', description: 'This is card number 9' },
    { label: "analysts", title: 'Card 10', description: 'This is card number 10' }
];

onMounted(() => {
    const cardType = route.params.name;
    cardList
        .filter(item => item.type === cardType)
        .forEach(item => cards.push(item))
});
</script>

<style scoped>

</style>
  