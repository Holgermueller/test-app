<template>
  <div id="Portfolio">
    <div class="image">
      <div class="caption">
        <span class="border">PORTFOLIO</span>
      </div>
    </div>

    <div class="portfolio-container">
      <v-container class="portfolio" fluid>
        <v-layout row wrap>
          <v-flex
            xs12
            sm12
            md6
            lg4
            xl4
            v-for="(Project, index) in Projects"
            :key="index"
          >
            <v-hover v-slot:default="{ hover }">
              <v-card class="project-card" tile :elevation="hover ? 12 : 2">
                <v-img class="card-image" :src="Project.image"></v-img>
                <v-card-title>
                  <div>{{ Project.title }}</div>
                </v-card-title>
                <v-card-text>
                  <p>{{ Project.description }}</p>
                  <p>Built with: {{ Project.tech }}</p>
                </v-card-text>
                <v-card-actions>
                  <a :href="Project.demoLink" target="_blank" class="demo">
                    <span class="mdi mdi-laptop-mac"></span>See the demo
                  </a>
                  <v-spacer></v-spacer>
                  <a :href="Project.repolink" target="_blank" class="repo">
                    <span class="mdi mdi-github"></span>See the repo
                  </a>
                </v-card-actions>
              </v-card>
            </v-hover>
          </v-flex>
        </v-layout>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  name: "Portfolio",

  data: () => ({
    Projects: [
      {
        title: "Trip Scheduler",
        description: "A way to keep track of any upcoming getaways.",
        image: require("../images/scheduler.png"),
        repolink: "https://github.com/Holgermueller/vue-train-scheduler",
        tech: "Vue, Vuex, Vuetify, Cloud Firestore",
        demoLink: "https://moodtracker-db661.web.app/?redirect=%2Fdashboard",
      },
      {
        title: "Hours Tracker",
        description:
          "A way for me to track hours I need to make up due to the bookstore closing early.",
        image: require("../images/hoursTracker.png"),
        repolink: "https://github.com/Holgermueller/vue-hours-tracker",
        tech: "Vue, Vuex, Vuetify, Cloud Firestore",
        demoLink: "https://trackmyhours-74a8f.web.app/",
      },
      {
        title: "Vue Wishlist",
        description:
          "Vue front-end and cloud firestore back-end. CRUD application. Gives users an alternative to using Amazon's wishlist as a way of tracking items they'd like to purchase, or have someone purchase for them.",
        image: require("../images/wishList.png"),
        repolink: "https://github.com/Holgermueller/wish-list",
        tech: "Vue, Vuex, Vuetify, Cloud Firestore",
        demoLink: "https://less-wish-list.web.app/dashboard",
      },
      {
        title: "Story-Idea Generator",
        description:
          "Single page application that helps stumped writers come up with their next best seller",
        image: require("../images/storyIdeaGenerator.png"),
        repolink: "https://github.com/Holgermueller/story-idea-generator",
        tech: "Gatsby, Material-Ui",
        demoLink: "https://holgermueller.github.io/story-idea-generator/",
      },
      {
        title: "Weather App",
        description:
          "A mobile responsive weather app with location search, which meets accessability standards.",
        image: require("../images/weatherapp.png"),
        repolink: "https://github.com/Holgermueller/weatherapp",
        tech: "VueJS, Vuex, OpenWeather API",
        demoLink: "https://holgermueller.github.io/weatherapp/",
      },
      {
        title: "Inspirational Thought Generator",
        description:
          "An app that gives users words of widsom to get them through the day. Thoughts can be shared on Twitter.",
        image: require("../images/inspthghtgnrtr.png"),
        repolink:
          "https://github.com/Holgermueller/Inspirational-thought-generator",
        tech: "jQuery, Grunt, Nodemon",
        demoLink: "https://inspirationalthoughtgenerator.herokuapp.com/",
      },
      {
        title: "Friend Finder",
        description: "A friend-finding app/ poor-man's dating app.",
        image: require("../images/friendfinder.png"),
        repolink: "https://github.com/Holgermueller/Friend_Finder",
        tech: "Expressjs, Nodemon, jQuery",
        demoLink: "https://friendfinderap.herokuapp.com/",
      },
    ],
  }),
};
</script>

<style scoped>
.image {
  /* image by Pixabay via Pexels */
  background-image: url("../images/portfoliobanner.png");
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
.portfolio-container {
  padding: 4%;
}
.portfolio {
  margin: auto;
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
