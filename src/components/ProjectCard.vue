<script>
import { ProjectCard } from '../assets/data/data';

export default {
    data() {
        return {
            projectCard: ProjectCard,
        };
    },
};
</script>
<template>
    <div>
        <div v-for="(card, index) in projectCard" :key="index">
            <img :src="card.img" alt="Project Image" />
            <h3>{{ card.title }}</h3>
            <p>{{ card.category }}</p>
            <div>{{ card.zoom }}</div>
        </div>
    </div>
</template>
<script></script>