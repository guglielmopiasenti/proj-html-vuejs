<script>

import PresentationCard from './PresentationCard.vue';
import AboutUs from './AboutUs.vue';
import AquaCard from './AquaCard.vue';
import ProjectCard from './ProjectCard.vue';
import TestimonialCard from './TestimonialCard.vue';
import BlogCard from './BlogCard.vue';
import GetStartedCard from './GetStartedCard.vue';
export default {
    components: { PresentationCard, AboutUs, ProjectCard, TestimonialCard, BlogCard, GetStartedCard, AquaCard }
}

</script>

<template>
    <section id="presentation">
        <PresentationCard title="OUR CONSULTANTS CAN HELP YOU" />
    </section>
    <section id="about-us">
        <AboutUs title="WE MAKE YOUR STRATEGY WORK"
            text="When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed when I hear the buzz of the little world among the stalks,and grow familiar indescribable forms of the insects .and flies, then I feel the presence of the Almighty . " />
    </section>
    <section id="a-card">
        <AquaCard title="WE HELP TO DELIVER THE BUSINESS CASE" text="When, while lovely valley teems with vapour around meand meridian sun strikes the upper impenetrable foliage of
            my trees, and but a thousand unknown" />
    </section>
    <section id="project">
        <ProjectCard title="OUR EXPERT TRUSTED CONSULTANTS HELP CLIENTS" />
    </section>
    <section id="testimonial">
        <TestimonialCard />
    </section>
    <section id="blog">
        <BlogCard />
    </section>
    <section id="get-started">
        <GetStartedCard title="LET'S TALK ABOUT WORK"
            par="A wonderful serenity has taken possession Far far away, behind the word mountains." />
    </section>
</template>

<style></style>