<script>
export default {
    name: 'Btn',
    props: {
        button: String
    }
};
</script>
<template>
    <button class="btn">
        {{ button }}
    </button>
</template>


<style lang="scss" scoped>
@use '../assets/scss/var' as *;

.btn {
    font-family: Raleway;
    position: relative;
    background-color: $c-a;
    border: none;
    letter-spacing: 4px;
    color: $c-g3;
    text-transform: uppercase;
    font-weight: 400;
    padding: 20px 35px;
    font-size: 16px;
    transition: color 0.5s ease;

    &:hover {
        color: white;
        background-color: $c-r;
    }
}
</style>