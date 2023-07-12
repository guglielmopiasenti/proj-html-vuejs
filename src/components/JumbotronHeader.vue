<script>
import Btn from '../components/AppButton.vue';
export default {
    components: {
        'btn': Btn
    },
    props: {
        button: String
    }
}

</script>

<template>
    <section id="jumbotron">
        <p>ALWAYS THE BEST WAY YOU NEED IT</p>
        <h1>THE BEST BUSINESS CONSULTING</h1>
        <div>
            <btn style="margin-right: 30px;" :button=button />
            <span class="fa-stack fa-2x">
                <i class="fa-regular fa-circle fa-stack-2x"></i>
                <i class="fa-sharp fa-solid fa-play fa-stack-1x"></i>
            </span>
        </div>

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

p {
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
    padding-bottom: 50px;
}

.fa-play {
    color: $c-a;
}
</style>