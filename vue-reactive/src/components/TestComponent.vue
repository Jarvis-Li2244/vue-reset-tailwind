
<template>
    <div class="card-page">
        <h1>Card Details</h1>
        <div class="card">
        <h3></h3>
        <p></p>
        </div>
    </div>
</template>

<script setup>
import { reactive, onMounted } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute()
const cards = reactive([]);

const cardList = [
    { name: "analysts", title: 'Card 1', description: 'This is card number 1' },
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
        .filter(item => item.name === cardName)
        .forEach(item => cards.push(item))
});
</script>

<style scoped>
.card {
    border: 1px solid #ddd;
    padding: 16px;
    margin: 8px;
    width: 200px;
}
</style>
  