<script>
export default {
    props: {
        title: String,
        par: String,
    }
}
</script>
<template>
    <div class="card-container">
        <h1>{{ title }}</h1>
        <p>{{ par }}</p>
    </div>
</template>


<style lang="scss" scoped> .card-container {
     background-image: url(../assets/img/business-people-working-together-on-project-and-B3MZ4TX.jpg);
     background-size: cover;
     background-repeat: no-repeat;
     padding: 150px 0;
     margin-top: 200px;
     text-align: center;
     color: white;

     h1 {
         font-size: 30px;
     }
 }
</style> 