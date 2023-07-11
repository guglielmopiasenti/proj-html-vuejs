<script>
import { BlogCard } from '../assets/data/data';

export default {
    data() {
        return {
            blogCard: BlogCard,
        };
    },
};
</script>
<template>
    <template>
        <div>
            <div v-for="(card, index) in blogCard" :key="index" class="blog-card">
                <img :src="card.img" alt="Blog Image" />
                <p>{{ card.date }}</p>
                <p>{{ card.author }}</p>
                <h3>{{ card.title }}</h3>
                <p>{{ card.text }}</p>
            </div>
        </div>
    </template>
</template>
<script>
</script>