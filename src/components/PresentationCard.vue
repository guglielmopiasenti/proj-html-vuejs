<script>
import { PresCard } from '../assets/data/data';
export default {
    props: {
        title: String
    },
    data() {
        return {
            presCard: PresCard,
        };
    }
}
</script>
<template>
    <div>
        <h1>{{ title }}</h1>
        <div v-for="(card, index) in presCard" :key="index">
            <img :src="card.img" alt="Card Image" />
            <h3>{{ card.title }}</h3>
            <p>{{ card.text }}</p>
        </div>
    </div>
</template>
<style></style>