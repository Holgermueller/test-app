<template>
  <div id="home">
    <Banner />
    <About class="page-section" />
    <Portfolio class="page-section" />
    <Education class="page-section" />
    <Connect class="page-section" />
    <TopButton />
  </div>
</template>

<script>
import Banner from "./Banner.vue";
import About from "./About.vue";
import Portfolio from "./Portfolio.vue";
import Education from "./Education.vue";
import Connect from "./Connect.vue";
import TopButton from "./TopButton.vue";

export default {
  name: "Index",

  components: {
    Banner,
    About,
    Portfolio,
    Education,
    Connect,
    TopButton,
  },
};
</script>

<style scoped>
.page-section {
  margin-top: 5rem;
  margin-bottom: 4rem;
}
</style>
