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
        <img src="../assets/img/business-people-working-together-on-project-and-5FHSKBL.jpg" alt="">
        <div>
            <div>ABOUT US</div>
            <h1>{{ title }}</h1>
            <p> {{ text }}
            </p>
        </div>
    </div>
</template>
<style></style>