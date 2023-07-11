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
</template>
<style lang="scss" scoped>
@use '../assets/scss/var' as *;
@use '../assets/scss/_mixins' as *;

h1 {
    @include container-md;
    padding-top: 50px;
    padding-bottom: 30px;
}

.card {
    @include container-md;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    width: calc(180% / 2);
    padding-bottom: 50px;



    img {
        background-color: $c-r;
        padding: 10px;
        border-radius: 50%;
    }

    p {
        padding-top: 10px;
    }
}

.card-container {
    display: flex;
    width: calc(100% / 2);
    align-items: flex-start;
    padding: 30px 100px;
}

.card-description {
    padding: 0 30px;
}
</style>