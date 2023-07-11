<script>

import NavbarHeader from './NavbarHeader.vue';
import JumbotronHeader from './JumbotronHeader.vue';

export default {
    components: { NavbarHeader, JumbotronHeader }
}

</script>

<template>
    <section id="header">
        <div class="container">
            <NavbarHeader />
            <JumbotronHeader />
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../assets/scss/var' as *;

#header {
    background-color: $c-g3;
    background-image: url(../assets/img/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg);
    background-position: 120% 0%, right;
    background-repeat: no-repeat;
    min-height: 120vh;
    background-size: 80%;
}

.container {
    width: 1300px;
    margin: 0 auto;
}
</style>