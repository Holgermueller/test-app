<template>
  <div id="home">
    <Banner />
    <About />
    <Skills />
    <Portfolio />
    <Education />
    <Connect />
    <TopButton />
  </div>
</template>

<script>
import Banner from "./Banner.vue";
import About from "./About.vue";
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
    Portfolio,
    Skills,
    Education,
    Connect,
    TopButton,
  },
};
</script>
