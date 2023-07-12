<script>
import Btn from '../components/AppButton.vue';
export default {
    components: {
        'btn': Btn
    },
    props: {
        title: String,
        text: String,
        button: String,
    }
}
</script>
<template>
    <div>
        <h1>{{ title }}</h1>
        <p>{{ text }}</p>
        <btn :button=button class="btn" />
    </div>
</template>
<style lang="scss" scoped>
@use '../assets/scss/var' as *;
@use '../assets/scss/mixins' as *;

div {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: right auto;
    width: 95%;
    padding: 100px 50px;
    background-color: $c-a;
    gap: 100px;

    h1 {
        @include second-font;
        font-size: 30px;
        width: 30%;
    }

    p {
        letter-spacing: 1px;
        line-height: 25px;
        width: 40%;
    }

    .btn {
        position: absolute;
        bottom: 0;
        right: 0;
        background-color: $c-r;
        color: white;

        &:hover {
            color: white;
            background-color: $c-g3;
        }
    }
}
</style>