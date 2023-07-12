<script>
export default {
    props: {
        title: String,
        text: String,
    }
}

</script>
<template>
    <div class="card-container">
        <img src="../assets/img/business-people-working-together-on-project-and-5FHSKBL.jpg" alt="">
        <div class="card-description">
            <div id="about">ABOUT US</div>
            <h1>{{ title }}</h1>
            <p> {{ text }}
            </p>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../assets/scss/mixins' as *;
@use '../assets/scss/var' as *;

.card-container {
    display: flex;
    align-items: center;
    background-color: $c-g3;
    color: white;


    img {
        max-height: 700px;
    }
}

#about {
    position: relative;
    padding-left: 80px;
    letter-spacing: 3px;

    &::after {
        content: '';
        position: absolute;
        top: 50%;
        left: 0;
        width: 60px;
        height: 3px;
        background-color: $c-a;
        transform: translateY(-50%);
    }
}

.card-description {
    padding: 50px;

    h1 {
        @include second-font;
        font-size: 50px;
        padding: 30px 0;
    }

    p {
        letter-spacing: 1px;
    }
}
</style>