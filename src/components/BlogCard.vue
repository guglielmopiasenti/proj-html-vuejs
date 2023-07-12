<script>
import Btn from '../components/AppButton.vue';
import { BlogCard } from '../assets/data/data';

export default {
    components: {
        'btn': Btn
    },
    props: {
        title: String,
        button: String,
    },
    data() {
        return {
            blogCard: BlogCard,
        };
    },
};
</script>
<template>
    <div class="container">
        <div>
            <div class="blog">BLOG</div>
            <h1>{{ title }}</h1>
        </div>
        <div>
            <btn :button=button />
        </div>
    </div>
    <div class="blog-container">
        <div v-for="(card, index) in blogCard" :key="index" class="blog-card">
            <div class="blog-img" :style="{ backgroundImage: `url(${card.img})` }"></div>
            <div class="blog-content">
                <div class="info">
                    <p>{{ card.date }}</p>
                    <p>{{ card.author }}</p>
                </div>
                <h2>{{ card.title }}</h2>
                <p class="text">{{ card.text }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../assets/scss/mixins' as *;
@use '../assets/scss/var' as *;

.container {
    @include container-lg;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.blog {
    color: white;
    letter-spacing: 3px;
    position: relative;
    padding-left: 40px;
    padding-bottom: 20px;

    &::after {
        content: '';
        position: absolute;
        top: 20%;
        left: 0;
        width: 30px;
        height: 3px;
        background-color: $c-a;
        transform: translateY(-50%);
    }
}

h1 {
    @include second-font;
    font-size: 40px;
    color: white;
    padding-bottom: 50px;
}

h2 {
    padding: 20px 0;
}

.text {
    letter-spacing: 1px;
    line-height: 25px;
    color: grey;
}

.blog-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    padding-bottom: 100px;
}

.blog-card {
    position: relative;
    width: 650px;
    height: 450px;
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
        height: 60%;
        background-color: white;
        padding: 30px;
        box-sizing: border-box;
        overflow: auto;

        .info {
            display: flex;
            gap: 20px;
            color: $c-r;
        }
    }
}
</style>
