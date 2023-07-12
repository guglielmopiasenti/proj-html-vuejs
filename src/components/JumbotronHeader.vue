<script>
export default {

}

</script>

<template>
    <section id="jumbotron">
        <div>ALWAYS THE BEST WAY YOU NEED IT</div>
        <h1>THE BEST BUSINESS CONSULTING</h1>
        <a href="#" class="btn btn-a">READ MORE</a>
    </section>
</template>

<style lang="scss" scoped>
@use '../assets/scss/mixins' as *;
@use '../assets/scss/var' as *;

#jumbotron {
    padding: 250px 0;
    width: 50%;
    color: white;
}

div {
    position: relative;
    font-size: 15px;
    font-weight: 300;
    letter-spacing: 4px;
    padding-left: 90px;

    &::after {
        content: '';
        position: absolute;
        top: 50%;
        left: 0;
        width: 75px;
        height: 3px;
        background-color: $c-a;
        transform: translateY(-50%);
    }
}

h1 {
    @include second-font;
    font-size: 100px;
    line-height: 90px;
    font-weight: 700;
}
</style>