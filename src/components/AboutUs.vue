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
            <div>ABOUT US</div>
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

.card-description {
    padding: 50px;

    h1 {
        font-size: 50px;
        padding: 30px 0;
    }
}
</style>