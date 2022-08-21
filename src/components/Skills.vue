<template>
  <div id="Skills">
    <div class="image">
      <div class="caption">
        <span class="border">SKILLS</span>
      </div>
    </div>

    <div class="skills-section">
      <v-card class="skills-card">
        <v-card-text>
          <div class="list">
            <ul v-for="(language, i) in languages" :key="i">
              <li>{{ language }}</li>
            </ul>
          </div>
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "MySkills",
  data: () => ({
    languages: ["javascript", "html", "css", "sql", "java", "python"],
    frameworks: ["react", "vue", "spring boot"],
  }),
};
</script>

<style scoped>
.image {
  /* Photo by Nemuel Sereti: https://www.pexels.com/photo/programming-language-on-a-screen-6424586/ via Pexels */
  background-image: url("../images/skills.png");
  background-size: cover;
  height: 500px;
  width: 100%;
}
.caption {
  width: 100%;
  position: relative;
  left: 0;
  top: 50%;
  text-align: center;
  color: black;
}
.caption span.border {
  background-color: white;
  color: #31708e;
  width: fit-content;
  font-size: 25px;
  padding: 18px;
  letter-spacing: 10px;
}
.skills-card {
  width: 75%;
  margin: 5% auto;
}
.list {
  width: 33%;
}
</style>
