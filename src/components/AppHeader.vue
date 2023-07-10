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
}

.container {
    width: 1200px;
    margin: 0 auto;
}
</style>