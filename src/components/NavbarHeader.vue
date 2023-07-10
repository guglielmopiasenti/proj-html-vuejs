<script>
import { NavLink } from '../assets/data/data';
export default {
    data() {
        return {
            navLinks: NavLink
        };
    }
}

</script>

<template>
    <img src="../assets/img/logotype.png" alt="">
    <div>
        <ul>
            <li v-for="(navItem, index) in navLinks" :key="index">
                {{ navItem.link }}
            </li>
        </ul>
    </div>
</template>

<style lang="scss"></style>