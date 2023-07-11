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

div {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: right auto;
    width: 80%;
    padding: 50px 50px;
    background-color: $c-a;


}
</style>