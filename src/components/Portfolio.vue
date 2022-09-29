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
            <div class="portfolio-card">
              <div class="card-inner">
                <div class="card-front">
                  <v-img
                    min-height="300"
                    min-width="300"
                    class="card-image"
                    :alt="Project.title"
                    :src="Project.image"
                  ></v-img>
                </div>
                <div class="card-back">
                  <v-card elevation="0">
                    <v-card-title> {{ Project.title }} </v-card-title>
                    <v-card-text>
                      <p class="project-description">
                        {{ Project.description }}
                      </p>
                      <p class="project-tools">
                        Built with: {{ Project.tech }}
                      </p>
                    </v-card-text>
                    <v-card-actions>
                      <a :href="Project.demoLink" target="_blank" class="demo">
                        <span class="mdi mdi-laptop"> Demo</span>
                      </a>
                    </v-card-actions>
                    <v-card-actions>
                      <!-- <a :href="Project.demoLink" target="_blank" class="demo">
                        <span class="mdi mdi-laptop"> Demo</span>
                      </a>
                      <v-spacer></v-spacer> -->

                      <a :href="Project.repolink" target="_blank" class="repo">
                        <span class="mdi mdi-github"> Repo</span>
                      </a>
                    </v-card-actions>
                  </v-card>
                </div>
              </div>
            </div>
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
        title: "QR Coder",
        description: "A static app that generates downloadable qr codes.",
        image: require("../images/qrcode.png"),
        repolink: "https://github.com/Holgermueller/qrcoder",
        tech: "Vanills JS, Bootstrap, Three JS, QRCode.js",
        demoLink: "https://holgermueller.github.io/qrcoder/",
      },
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
          "Vue and cloud firestore CRUD application. Gives users an alternative to a major e-commerce site's wish list feature.",
        image: require("../images/wishList.png"),
        repolink: "https://github.com/Holgermueller/wish-list",
        tech: "Vue, Vuex, Vuetify, Cloud Firestore",
        demoLink: "https://less-wish-list.web.app/dashboard",
      },
      {
        title: "Story-Idea Generator",
        description:
          "Single page application that helps stumped writers create their next best-seller.",
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
        title: "ITG",
        description:
          "An app that gives users words of widsom to get them through the day. The wisdom can be shared on Twitter.",
        image: require("../images/itg.jpg"),
        repolink: "https://github.com/Holgermueller/ITG",
        tech: "Postcss, javascript",
        demoLink: "https://holgermueller.github.io/ITG/",
      },
      {
        title: "Friend Finder",
        description: "A friend-finding app/ poor-man's dating app.",
        image: require("../images/friendfinder.png"),
        repolink: "https://github.com/Holgermueller/Friend_Finder",
        tech: "Expressjs, Nodemon, jQuery",
        demoLink: "https://friend-finder.onrender.com/home",
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
  width: 85%;
}
.portfolio-card {
  background-color: transparent;
  padding: 0;
  margin: 10px;
  perspective: 1000px;
  border: 1px solid #f3f3f3;
  border-radius: 5px;
  min-width: 300px;
  min-height: 300px;
}
.card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  transition: transform 1s;
  transform-style: preserve-3d;
  border-radius: 5px;
}
.portfolio-card:hover .card-inner {
  transform: rotateY(180deg);
  transition: transform 0.5s;
}
.card-front,
.card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  border-radius: 5px;
}
.card-front {
  height: 100%;
  width: 100%;
  background-color: #bbb;
  color: black;
}
.card-image {
  height: 100%;
  width: 100%;
}
.card-back {
  transform: rotateY(180deg);
  background-color: #f3f3f3;
}
.v-card__actions {
  justify-content: center;
}
a,
.demo,
.repo {
  text-decoration: none;
  margin: 4px;
  color: #000000;
  font-size: 1.5rem;
  position: relative;
  text-align: center;
}

a:hover {
  cursor: pointer;
  color: blue;
}

@media (min-width: 360px) and (max-width: 450px) {
  .portfolio-container {
    width: 90%;
  }
}
</style>
