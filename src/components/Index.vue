<template>
  <div id="home">
    <Banner />
    <About />
    <Skills />
    <Experience />
    <Portfolio />
    <Education />
    <Connect />
    <TopButton />
  </div>
</template>

<script>
import Banner from "./Banner.vue";
import About from "./About.vue";
import Experience from "./Experience.vue";
import Portfolio from "./Portfolio.vue";
import Skills from "./Skills.vue";
import Education from "./Education.vue";
import Connect from "./Connect.vue";
import TopButton from "./TopButton.vue";

export default {
  name: "Index",

  components: {
    Banner,
    About,
    Experience,
    Portfolio,
    Skills,
    Education,
    Connect,
    TopButton,
  },
};
</script>
