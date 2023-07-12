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
    <div class="blog-container">
        <div v-for="(card, index) in blogCard" :key="index" class="blog-card">
            <div class="blog-img" :style="{ backgroundImage: `url(${card.img})` }"></div>
            <div class="blog-content">
                <p>{{ card.date }}</p>
                <p>{{ card.author }}</p>
                <h3>{{ card.title }}</h3>
                <p>{{ card.text }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.blog-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
}

.blog-card {
    position: relative;
    width: 600px;
    height: 400px;
    margin: 10px;

    .blog-img {
        width: 100%;
        height: 100%;
        background-size: cover;
        background-position: center;
    }

    .blog-content {
        position: absolute;
        bottom: -25%;
        right: 0%;
        width: 80%;
        height: 50%;
        background-color: white;
        padding: 10px;
        box-sizing: border-box;
        overflow: auto;
    }
}
</style>
