<template>
  <div>
    <HeaderOne showHeaderTop="true" />
    <Hero />
    <YogaAbout />
    <Course />
    <FunFact />
    <WhyChoose />
    <Instructor />
    <Instagram />
    <FooterYoga />
    <ScrollToTop />
  </div>
</template>

<script lang="ts">
import FooterYoga from "../footer/FooterYoga.vue";
import Hero from "./Hero.vue";
import Instructor from "./Instructor.vue";
import WhyChoose from "./WhyChoose.vue";
import Instagram from "./Instagram.vue";
import HeaderOne from "../header/HeaderOne.vue";
import FunFact from "./FunFact.vue";
import ScrollToTop from "../footer/ScrollToTop.vue";
import Course from "./Course.vue";
import YogaAbout from "./YogaAbout.vue";

export default {
  name: "app",
  components: {
    FooterYoga,
    Hero,
    WhyChoose,
    Instructor,
    Instagram,
    HeaderOne,
    Course,
    FunFact,
    ScrollToTop,
    YogaAbout,
  },
};
</script>

<style scoped></style>
