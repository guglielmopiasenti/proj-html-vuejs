<script>
export default {
    props: {
        title: String,
        text: String,
    }
}
</script>
<template>
    <div>
        <h1>{{ title }}</h1>
        <p>{{ text }}</p>
    </div>
</template>
<style lang="scss" scoped>
@use '../assets/scss/var' as *;
@use '../assets/scss/mixins' as *;

div {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: right auto;
    width: 90%;
    padding: 100px 50px;
    background-color: $c-a;

    h1 {
        @include second-font;
        font-size: 35px;
    }

    p {
        letter-spacing: 1px;
    }

}
</style>