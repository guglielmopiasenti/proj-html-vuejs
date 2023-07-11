<script>

import PresentationCard from './PresentationCard.vue';
import AboutUs from './AboutUs.vue';
import ProjectCard from './ProjectCard.vue';
import TestimonialCard from './TestimonialCard.vue';
import BlogCard from './BlogCard.vue';
export default {
    components: { PresentationCard, AboutUs, ProjectCard, TestimonialCard, BlogCard }
}

</script>

<template>
    <section id="presentation">
        <h2>OUR CONSULTANTS CAN HELP YOU</h2>
        <PresentationCard />
    </section>
    <section id="about-us">
        <AboutUs />
    </section>
    <section id="a-card">

    </section>
    <section id="project">
        <ProjectCard />
    </section>
    <section id="testimonial">
        <TestimonialCard />
    </section>
    <section id="blog">
        <BlogCard />
    </section>
    <section id="get-started"></section>
</template>

<style></style>