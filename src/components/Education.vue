<template>
  <div id="Education">
    <div class="image">
      <div class="caption">
        <span class="border">EDUCATION</span>
      </div>
    </div>
    <div class="education-container">
      <div v-for="(item, index) in education" :key="index">
        <v-card class="education-card" tile>
          <v-card-title>
            <h1 class="headline">
              {{ item.school }}
            </h1>
          </v-card-title>
          <v-card-text>
            <h2 class="title">
              {{ item.program }}
            </h2>
          </v-card-text>
        </v-card>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Education",

  data: () => ({
    education: [
      { school: "Google", program: "UX Design Certificate" },
      {
        school: "freeCodeCamp",
        program: "Javascript Algorithms and Data Structures",
      },
      {
        school: "Wes Bos",
        program: "JavaScript30",
      },
      {
        school: "University of Minnesota College of Continuing Education",
        program: "Full-stack Web Developer Certificate",
      },
      {
        school: "SUNY New Paltz",
        program: "Master's English",
      },
      {
        school: "SUNY New Paltz",
        program: "Bachelor's Creative Writing",
      },
    ],
  }),
};
</script>

<style scoped>
#Education {
  background-color: rgb(49, 112, 142, 0.3);
}
.image {
  /* image by Pixabay via Pexels */
  background-image: url("../images/education.png");
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
  color: black;
  width: fit-content;
  font-size: 25px;
  padding: 18px;
  letter-spacing: 10px;
}
.education-container {
  padding: 5%;
}
.education-card {
  width: 55%;
  margin: 1px auto;
}
</style>
