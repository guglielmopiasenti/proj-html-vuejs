<script>
import Btn from '../components/AppButton.vue';
export default {
    components: {
        'btn': Btn
    },
    props: {
        title: String,
        par: String,
        button: String
    }
}
</script>
<template>
    <div class="card-container">
        <h1>{{ title }}</h1>
        <p>{{ par }}</p>
        <btn :button=button class="btn" />
    </div>
</template>


<style lang="scss" scoped> @use '../assets/scss/var' as *;

 .card-container {
     background-image: url(../assets/img/business-people-working-together-on-project-and-B3MZ4TX.jpg);
     background-size: contain;
     background-repeat: no-repeat;
     padding: 100px 0;
     margin-top: 200px;
     text-align: center;
     color: white;

     h1 {
         font-size: 50px;
     }

     p {
         letter-spacing: 1px;
         padding: 30px 0;
     }

     .btn {
         background-color: $c-g3;
         color: white;

         &:hover {
             color: $c-g3;
             background-color: $c-a;
         }
     }
 }
</style> 