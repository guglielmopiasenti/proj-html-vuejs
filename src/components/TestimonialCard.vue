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
    <div class="card-container">
        <div v-for="(card, index) in testimonialCard" :key="index" class="testimonial-card">
            <div class="testimonial-content">
                <p>{{ card.text }}</p>
                <p>{{ card.author }}</p>
                <p>{{ card.company }}</p>
            </div>
            <div class="testimonial-img" :style="{ backgroundImage: `url(${card.img})` }"></div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../assets/scss/var' as *;

.card-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-end;

    .testimonial-card {
        position: relative;
        width: 300px;
        height: 300px;
        background-color: white;
        overflow: hidden;

        .testimonial-img {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-size: cover;
            background-position: center;
            opacity: 0;
            transition: opacity 0.5s ease;
        }

        &:hover {
            .testimonial-img {
                opacity: 1;
            }
        }

        .testimonial-content {
            position: relative;
            z-index: 2;
            padding: 20px;
        }
    }
}
</style>
