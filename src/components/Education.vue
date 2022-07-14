<template>
  <div id="Education">
    <h1 class="section-header">Education</h1>
    <div v-for="(item, index) in education" :key="index">
      <v-card class="education-card" tile>
        <v-card-title>
          {{ item.school }}
        </v-card-title>
        <v-card-text>
          {{ item.program }}
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "Education",

  data: () => ({
    education: [
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
.section-header {
  text-align: center;
}
.education-card {
  width: 55%;
  margin: 1px auto;
}
</style>
