<template>
  <v-app>
    <v-app-bar v-if="$vuetify.breakpoint.mobile" app color="#31708e" dark>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <div class="align-center">
        <h1 class="brand" @click.prevent="scrollToTop">Holger Mueller</h1>
      </div>
    </v-app-bar>

    <v-app-bar v-else app color="#31708e" dark>
      <div class="d-flex align-center">
        <h1 class="brand" @click.prevent="scrollToTop">Holger Mueller</h1>
      </div>

      <v-spacer></v-spacer>

      <div v-for="(section, index) in sections" :key="index">
        <v-btn
          :id="section.link"
          @click.prevent="scrollToSection(section)"
          text
        >
          <span class="mr-2"> {{ section.title }}</span>
        </v-btn>
      </div>
    </v-app-bar>

    <v-navigation-drawer
      width="50%"
      v-model="drawer"
      color="#31708e"
      fixed
      temporary
    >
      <v-list nav dense>
        <v-list-item class="close" @click.prevent="drawer = !drawer" dark>
          <v-icon x-large>mdi-close</v-icon>
        </v-list-item>

        <v-list-item
          @click="drawer = !drawer"
          v-for="(section, index) in sections"
          :key="index"
          dark
          link
        >
          <v-btn
            :id="section.link"
            @click.prevent="scrollToSection(section)"
            text
          >
            <span class="white--text headline"> {{ section.title }} </span>
          </v-btn>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <Index />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import Index from "./components/Index.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",

  components: {
    Index,
    Footer,
  },

  data: () => ({
    drawer: false,
    sections: [
      {
        title: "About",
        link: "#About",
      },
      { title: "Skills", link: "#Skills" },
      { title: "Portfolio", link: "#Portfolio" },
      {
        title: "Education",
        link: "#Education",
      },
      { title: "Connect", link: "#Connect" },
    ],
  }),

  methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" });
    },

    scrollToSection(section) {
      const position = this.$el.querySelector(section.link).offsetTop;

      requestAnimationFrame(() => {
        window.scrollTo({ top: position, behavior: "smooth" });
      });
    },
  },
};
</script>

<style scoped>
.brand:hover,
a:hover {
  cursor: pointer;
}

a {
  text-decoration: none;
  color: white;
}
</style>
