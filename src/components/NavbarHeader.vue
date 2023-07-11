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
    <nav>
        <img src="../assets/img/logotype.png" alt="">
        <div>
            <ul>
                <li v-for="(navItem, index) in navLinks" :key="index">
                    {{ navItem.link }}
                </li>
            </ul>
        </div>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 30px 0;
}

img {
    height: 20px
}

ul {
    display: flex;
    gap: 35px;
    color: white;
}
</style>