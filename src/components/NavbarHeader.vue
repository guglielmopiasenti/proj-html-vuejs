<script>
import { NavLink } from '../assets/data/data';
export default {
    data() {
        return {
            navLinks: NavLink
        };
    },
    methods: {
        activateLink(index) {
            this.navLinks.forEach((link, i) => {
                this.navLinks[i].active = i === index;
            });
        },
        resetActiveLink() {
            this.navLinks.forEach((link, i) => {
                this.navLinks[i].active = i === 0;
            });
        }
    }
}
</script>


<template>
    <nav>
        <img src="../assets/img/logotype.png" alt="">
        <div>
            <ul>
                <li v-for="(navItem, index) in navLinks" :key="index" :class="{ active: navItem.active }"
                    @mouseover="activateLink(index)" @mouseleave="resetActiveLink()">
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
    height: 20px;
}

ul {
    display: flex;
    gap: 35px;
    font-weight: 200;
    color: white;

    .active {
        font-weight: 500;

        &::before {
            content: '';
            position: absolute;
            top: -30px;
            left: 0;
            width: 100%;
            height: 2px;
            background: white;
        }
    }

    li {
        position: relative;

        &::before {
            content: '';
            position: absolute;
            top: -30px;
            left: 0;
            width: 0;
            height: 2px;
            background: white;
            transition: width 0.3s ease;
        }

        &:hover {
            &::before {
                width: 100%;
            }
        }
    }
}
</style>
