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
            md12
            lg12
            xl12
            v-for="(Job, index) in Jobs"
            :key="index"
          >
            <v-card class="experience-card">
              <v-img class="card-image" :alt="Job.title" :src="Job.image">
              </v-img>

              <div id="overlay">
                <v-dialog v-model="dialog" width="500">
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      class="info-button white--text"
                      v-bind="attrs"
                      v-on="on"
                      color="#31708e"
                      x-large
                    >
                      {{ Job.title }}
                    </v-btn>
                  </template>

                  <v-card>
                    <v-img :alt="Job.title" :src="Job.image"></v-img>
                    <v-card-title>
                      {{ Job.title }}
                    </v-card-title>
                    <v-card-subtitle class="timeline">
                      Timeline: {{ Job.time }}
                    </v-card-subtitle>
                    <v-card-text>
                      <p class="description">{{ Job.description }}</p>
                      <p class="description">Tech used: {{ Job.tech }}</p>
                      <p class="description">For more info:</p>
                    </v-card-text>
                    <v-card-actions>
                      <v-btn
                        elevation="0"
                        :href="Job.repolink"
                        target="_blank"
                        color="#31708e"
                        class="white--text"
                        x-large
                        >Repo</v-btn
                      >
                      <v-spacer></v-spacer>
                      <v-btn
                        @click="dialog = false"
                        elevation="0"
                        color="#31708e"
                        class="white--text"
                        x-large
                        >Close</v-btn
                      >
                      <v-spacer></v-spacer>
                      <v-btn
                        elevation="0"
                        :href="Job.demoLink"
                        target="_blank"
                        x-large
                        color="#31708e"
                        class="white--text"
                        >See the Site</v-btn
                      >
                    </v-card-actions>
                  </v-card>
                </v-dialog>
              </div>
            </v-card>
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
    overlay: false,
    dialog: false,
    Jobs: [
      {
        title: "Community Justice Investigations",
        time: "Aug. 2023 - Oct. 2023",
        description:
          "A website I built for the Community Justice Investigations, a 501(c)(3) non-profit operating in the Minneapolis-St Paul Metro area.",
        image: require("../images/cji.png"),
        repolink: "https://github.com/Holgermueller/cji",
        tech: "Wordpress, Elementor",
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

.experience-card {
  position: relative;
}

#overlay {
  position: absolute;
  bottom: 0;
  background: rgb(0, 0, 0);
  background: rgba(0, 0, 0, 0.5);
  color: #f1f1f1;
  width: 100%;
  height: 100%;
  transition: 0.5s ease;
  opacity: 0;
  color: white;
  text-align: center;
}

.experience-card:hover #overlay {
  opacity: 1;
}

.info-button {
  top: 45%;
}

.timeline {
  font-size: 1rem;
}

.description {
  font-weight: bold;
  font-size: 1.25rem;
  padding: 4px 0;
}
</style>
