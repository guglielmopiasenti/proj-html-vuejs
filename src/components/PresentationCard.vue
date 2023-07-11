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
    <div class="card">
        <h1>{{ title }}</h1>
        <div v-for="(card, index) in presCard" :key="index">
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

.card {
    @include container-md;
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    width: calc(100% / 2);
    padding: 10px;

    h1 {
        padding: 50px 0;
    }

    img {
        background-color: $c-r;
        padding: 10px;
        border-radius: 50%;
    }
}

.card-description {

    padding-left: 50px;
}
</style>