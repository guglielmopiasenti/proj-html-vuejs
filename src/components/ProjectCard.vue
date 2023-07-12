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
                    <div>
                        PROJECT
                    </div>
                    <div>{{ title }}</div>
                    <div></div>
                </div>
            </div>
            <div class="card-components">
                <div v-for="(card, index) in projectCard" :key="index">
                    <img :src="card.img" alt="Project Image" />
                    <div>
                        <h3>{{ card.title }}</h3>
                        <p>{{ card.category }}</p>
                        <div>{{ card.zoom }}</div>
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
    @include container-md
}

.card-components {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    padding: 30px 0;

    img {
        width: 350px;
    }
}
</style>