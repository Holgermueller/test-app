<template>
  <div id="home">
    <Banner />
    <About class="page-section" />
    <Portfolio class="page-section" />
    <Connect class="page-section" />
  </div>
</template>

<script>
import Banner from "./Banner.vue";
import About from "./About.vue";
import Portfolio from "./Portfolio.vue";
import Connect from "./Connect.vue";

export default {
  name: "Index",

  components: {
    Banner,
    About,
    Portfolio,
    Connect,
  },
};
</script>

<style scoped>
.page-section {
  margin-top: 5rem;
  margin-bottom: 4rem;
}
</style>
