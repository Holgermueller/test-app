<template>
  <div id="portfolio">
    <h1 class="section-header">Portfolio</h1>
  </div>
</template>

<script>
export default {
  name: "Portfolio",

  data() {
    return {
      Projects: [],
    };
  },
};
</script>

<style scoped>
#Portfolio {
  background-color: #8fc1e3;
  width: 100%;
}
.section-header {
  text-align: center;
  padding-top: 7%;
}
.portfolio-container {
  width: 75%;
}
.project-card {
  margin: 8px;
}
.card-image {
  height: 250px;
  width: 100%;
}
a {
  text-decoration: none;
}
a:hover {
  cursor: pointer;
  color: blue;
}
.demo,
.repo {
  color: black;
}
@media (min-width: 360px) and (max-width: 450px) {
  .portfolio-container {
    width: 90%;
  }
}
</style>
