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
    <div class="background">
        <h1>{{ title }}</h1>
        <div class="card">
            <div class="card-container" v-for="(card, index) in presCard" :key="index">
                <img :src="card.img" alt="Card Image" />
                <div class="card-description">
                    <h3>{{ card.title }}</h3>
                    <p>{{ card.text }}</p>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../assets/scss/var' as *;
@use '../assets/scss/_mixins' as *;

.background {
    background-color: white;
}

h1 {
    @include container-md;
    @include second-font;
    position: relative;
    padding-top: 80px;
    padding-bottom: 30px;

    &::after {
        content: '';
        position: absolute;
        top: 68%;
        right: -16%;
        width: 70%;
        height: 3px;
        background-color: $c-a;
        transform: translateY(-50%);
    }
}

.card {
    @include container-md;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    width: calc(180% / 2);
    padding-bottom: 50px;

    h3 {
        @include second-font;
    }

    img {
        background-color: $c-r;
        padding: 10px;
        border-radius: 50%;
    }

    p {
        padding-top: 10px;
        font-weight: 200;
        letter-spacing: 1px;
    }
}

.card-container {
    display: flex;
    width: calc(100% / 2);
    align-items: flex-start;
    padding: 80px 100px;
}

.card-description {
    padding: 0 30px;
}
</style>