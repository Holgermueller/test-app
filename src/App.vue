<template>
  <v-app>
    <v-app-bar v-if="$vuetify.breakpoint.mobile" app color="#31708e" dark>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <div class="align-center">
        <h1 class="brand">Holger Mueller</h1>
      </div>
    </v-app-bar>

    <v-app-bar v-else app color="#31708e" dark>
      <div class="d-flex align-center">
        <h1 class="brand" @click.prevent="scrollToTop">Holger Mueller</h1>
      </div>

      <v-spacer></v-spacer>

      <div v-for="(section, index) in sections" :key="index">
        <v-btn :id="index" :href="section.link" text>
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
        <v-list-item class="close" @click="drawer = !drawer" dark>
          <v-icon x-large>mdi-close</v-icon>
        </v-list-item>

        <v-list-item
          @click="drawer = !drawer"
          v-for="(section, index) in sections"
          :key="index"
          dark
          link
        >
          <v-btn :href="section.link" text>
            <span class="white--text headline"> {{ section.title }} </span>
          </v-btn>
          <!-- <v-list-item-content>
            <v-list-item-title>
              <span class="white--text headline"> {{ section.title }} </span>
            </v-list-item-title>
          </v-list-item-content> -->
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
        icon: "mdi mdi-book-open-page-variant",
        link: "#About",
      },
      { title: "Skills", icon: "mdi mdi-arrow-up", link: "#Skills" },
      { title: "Portfolio", icon: "mdi mdi-iframe", link: "#Portfolio" },

      {
        title: "Education",
        icon: "",
        link: "#Education",
      },
      { title: "Connect", icon: "mdi mdi-laptop-mac", link: "#Connect" },
    ],
  }),

  methods: {
    scrollToTop() {
      window.scrollTo(0, 0);
    },
  },
};
</script>

<style scoped>
.brand:hover {
  cursor: pointer;
}

a {
  text-decoration: none;
  color: white;
}
</style>
