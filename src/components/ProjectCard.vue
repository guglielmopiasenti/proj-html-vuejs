<script>
import { ProjectCard } from '../assets/data/data';

export default {
    props: {
        title: String
    },
    data() {
        return {
            projectCard: ProjectCard,
        };
    },
};
</script>
<template>
    <div class="background">
        <div class="section-container">
            <div>
                <div>
                    <div id="project">
                        PROJECT
                    </div>
                    <h1>{{ title }}</h1>
                    <div></div>
                </div>
            </div>
            <div class="card-components">
                <div v-for="(card, index) in projectCard" :key="index" class="card">
                    <img :src="card.img" alt="Project Image" />
                    <div class="overlay">
                        <div>
                            <h3>{{ card.title }}</h3>
                            <p>{{ card.category }}</p>
                        </div>
                        <div class="zoom">{{ card.zoom }}</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped >
@use '../assets/scss/mixins' as *;
@use '../assets/scss/var' as *;

.background {
    background-color: $c-g3;
}

.section-container {
    @include container-lg;
    color: white;
    padding: 180px 0;

    #project {
        letter-spacing: 1px;
        position: relative;
        padding-left: 80px;

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

    h1 {
        @include second-font;
        font-size: 40px;
        width: 60%;
        padding: 30px 0;
    }

    h3 {
        font-weight: 600;
    }

    .zoom {
        font-size: 25px;
        background-color: $c-g3;
        padding: 10px 20px;
    }
}

.card-components {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    padding: 30px 0;

    .card {
        position: relative;

        img {
            width: 400px;
            transition: all .3s ease-in-out;
        }

        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            display: flex;
            align-items: flex-end;
            justify-content: space-between;
            opacity: 0;
            transition: opacity .3s ease-in-out;
            color: white;
            background: rgba(249, 30, 58, 0.5);
            padding: 20px;
        }

        &:hover {
            img {
                filter: brightness(.5);
            }

            .overlay {
                opacity: 1;
            }
        }
    }
}
</style>