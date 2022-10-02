<template>
  <div id="Skills">
    <div class="image">
      <div class="caption">
        <span class="border">SKILLS</span>
      </div>
    </div>

    <div class="skills-section">
      <v-card class="skills-card" elevation="0">
        <v-card-text>
          <v-container fluid>
            <v-layout row wrap>
              <v-flex xs12 sm12 md6 lg4 xl4>
                <v-card elevation="0">
                  <v-card-title>
                    <h1>UX/UI</h1>
                  </v-card-title>
                  <v-card-text>
                    <hr />
                    <ul v-for="(item, i) in designItems" :key="i">
                      <li class="body-1">
                        {{ item }}
                      </li>
                    </ul>
                  </v-card-text>
                </v-card></v-flex
              >
              <v-flex xs12 sm12 md6 lg4 xl4>
                <v-card elevation="0">
                  <v-card-title>
                    <h1>Frontend</h1>
                  </v-card-title>
                  <v-card-text>
                    <hr />
                    <ul v-for="(item, i) in frontendItems" :key="i">
                      <li class="body-1">
                        {{ item }}
                      </li>
                    </ul>
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 sm12 md6 lg4 xl4>
                <v-card elevation="0">
                  <v-card-title>
                    <h1>Backend</h1>
                  </v-card-title>

                  <v-card-text>
                    <hr />
                    <ul v-for="(item, i) in backendItems" :key="i">
                      <li class="body-1">
                        {{ item }}
                      </li>
                    </ul>
                  </v-card-text>
                </v-card>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "MySkills",
  data: () => ({
    designItems: [
      "Pen & Paper",
      "Figma",
      "Adobe XD",
      "Defining user pain points",
      "Empathizing with users by creating empathy maps, personas, user stories, and user journey maps",
      "Crazy Eights",
      "How Might We",
      "Competitive audits",
      "Wireframes and prototypes on paper and digitally",
      "Considering accessibility at every point in the design process",
    ],
    frontendItems: [
      "Javascript",
      "HTML",
      "CSS",
      "Git",
      "ReactJS",
      "Vuejs",
      "Vuex",
      "Vuetify",
      "MaterialUI",
      "Bootstrap",
      "Postcss",
    ],
    backendItems: [
      "MongoDB",
      "Firebase/Cloud Firestore",
      "Thunder Client",
      "MySQL",
      "ExpressJS",
      "Markdown",
    ],
    devTools: ["VS Code", "Github", "Terminal"],
  }),
};
</script>

<style scoped>
#Skills {
  background-color: rgb(49, 112, 142, 0.3);
  padding-bottom: 5%;
}
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
  margin: auto;
}
ul {
  list-style: none;
  margin-top: 8px;
}

li {
  color: #080808;
}
</style>
