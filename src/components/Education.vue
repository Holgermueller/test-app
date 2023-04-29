<template>
  <div id="Education">
    <div class="image">
      <div class="caption">
        <span class="border">EDUCATION</span>
      </div>
    </div>
    <div class="education-container">
      <div v-for="(item, index) in education" :key="index">
        <v-card class="education-card" :class="item.class" tile>
          <v-card-title class="card-title">
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
    observerLeft: null,
    observerRight: null,
    education: [
      {
        school: "Google",
        program: "IT Support Specialization Certificate",
        class: "hidden-left",
      },
      {
        school: "Google",
        program: "UX/UI Design Certificate",
        class: "hidden-right",
      },
      {
        school: "freeCodeCamp",
        program: "Javascript Algorithms and Data Structures",
        class: "hidden-left",
      },
      {
        school: "Wes Bos",
        program: "JavaScript30",
        class: "hidden-right",
      },
      {
        school: "University of Minnesota College of Continuing Education",
        program: "Full-stack Web Developer Certificate",
        class: "hidden-left",
      },
      {
        school: "SUNY New Paltz",
        program: "Master's English",
        class: "hidden-right",
      },
      {
        school: "SUNY New Paltz",
        program: "Bachelor's Creative Writing",
        class: "hidden-left",
      },
    ],
  }),

  mounted() {
    this.observerLeft = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("show-left");
        } else {
          entry.target.classList.remove("show-left");
        }
      });
    });

    const hiddenLeftElements = document.querySelectorAll(".hidden-left");
    hiddenLeftElements.forEach((el) => this.observerLeft.observe(el));

    this.observerRight = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("show-right");
        } else {
          entry.target.classList.remove("show-right");
        }
      });
    });

    const hiddenRightElements = document.querySelectorAll(".hidden-right");
    hiddenRightElements.forEach((el) => this.observerRight.observe(el));
  },
};
</script>

<style scoped>
#Education {
  background-color: rgb(49, 112, 142, 0.3);
  white-space: break-spaces;
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
  width: 65%;
  margin: 4px auto;
}
.title {
  color: #080808;
}

.hidden-left {
  opacity: 0;
  filter: blur(5px);
  transform: translateX(-100%);
  transition: all 1s;
}

.show-left {
  opacity: 1;
  filter: blur(0);
  transform: translateX(0);
}

.hidden-right {
  opacity: 0;
  filter: blur(5px);
  transform: translateX(100%);
  transition: all 1s;
}

.show-right {
  opacity: 1;
  filter: blur(0);
  transform: translateX(0);
}

@media (prefers-reduced-motion) {
  .hidden-left {
    transition: none;
  }
}
</style>
