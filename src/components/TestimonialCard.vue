<script>
import { TestimonialCard } from '../assets/data/data';

export default {
    props: {
        title: String
    },
    data() {
        return {
            testimonialCard: TestimonialCard,
        };
    },
};
</script>
<template>
    <div class="container">
        <div class="testimonial">TESTIMONIAL</div>
        <h1>{{ title }}</h1>
        <div class="card-container">
            <div v-for="(card, index) in testimonialCard" :key="index" class="testimonial-card">
                <div class="testimonial-content">
                    <p>{{ card.text }}</p>
                    <h2>{{ card.author }}</h2>
                    <p>{{ card.company }}</p>
                </div>
                <div class="testimonial-img" :style="{ backgroundImage: `url(${card.img})` }"></div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../assets/scss/var' as *;
@use '../assets//scss/mixins' as *;

.container {
    .testimonial {
        position: relative;
        color: white;
        text-align: center;

        &::after {
            content: '';
            position: absolute;
            top: 68%;
            right: 35px;
            width: 70px;
            height: 3px;
            background-color: $c-a;
            transform: translateY(-50%);
        }
    }

    h1 {
        @include second-font;
        color: white;
        font-size: 40px;
        width: 40%;
        text-align: right;
        padding: 50px 0;
        translate: 145%;
    }

    h2 {
        @include second-font;
        padding: 40px 0;
    }

    p {
        letter-spacing: 1px;
        line-height: 25px;
        color: gray;
    }
}

.card-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-end;
    padding-bottom: 200px;

    .testimonial-card {
        position: relative;
        width: 450px;
        height: 450px;
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

            h2 {
                color: white;
            }

            p {
                color: white;
            }
        }

        .testimonial-content {
            position: relative;
            z-index: 2;
            padding: 60px;
        }
    }
}
</style>
