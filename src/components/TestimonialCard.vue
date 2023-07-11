<script>
import { TestimonialCard } from '../assets/data/data';

export default {
    data() {
        return {
            testimonialCard: TestimonialCard,
        };
    },
};
</script>
<template>
    <div>
        <div v-for="(card, index) in testimonialCard" :key="index" class="testimonial-card">
            <p>{{ card.text }}</p>
            <p>{{ card.author }}</p>
            <p>{{ card.company }}</p>
            <img :src="card.img" alt="Testimonial Image" />
        </div>
    </div>
</template>