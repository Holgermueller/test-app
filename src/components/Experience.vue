<template>
  <div id="Experience">
    <div class="image">
      <div class="caption">
        <span class="border">EXPERIENCE</span>
      </div>
    </div>

    <div class="experience-container">
      <v-container class="experience" fluid>
        <v-layout row wrap>
          <v-flex
            xs12
            sm12
            md6
            lg4
            xl4
            v-for="(Job, index) in Jobs"
            :key="index"
          >
            <div class="experience-card">
              <v-img
                class="card-image"
                :alt="Job.title"
                :src="Job.image"
              ></v-img>
            </div>
          </v-flex>
        </v-layout>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  name: "Experience",

  data: () => ({
    Jobs: [
      {
        title: "Community Justice Investigations",
        time: "Aug. 2023 - Oct. 2023",
        description:
          "A website I built for the Community Justice Investigations non-profit organization.",
        image: require("../images/cji.png"),
        repolink: "https://github.com/Holgermueller/cji",
        tech: "Wordpress",
        demoLink: "https://communityjusticeinvestigations.org/",
      },
    ],
  }),
};
</script>

<style>
.image {
  /* image by Lex Photography via Pexels */
  background-image: url("../images/experience.png");
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
  background-color: #31708e;
  color: white;
  width: fit-content;
  font-size: 25px;
  padding: 18px;
  letter-spacing: 10px;
}

.experience-container {
  padding: 4%;
}

.experience {
  margin: auto;
  width: 85%;
}
</style>
