<template>
  <v-app>
    <v-app-bar app color="#31708e" dark>
      <div class="d-flex align-center">
        <h1 class="brand" @click.prevent="scrollToTop">Holger Mueller</h1>
      </div>

      <v-spacer></v-spacer>

      <div v-for="(section, index) in sections" :key="index">
        <v-btn :id="index" :href="section.link" text block>
          <span class="mr-2"> {{ section.title }}</span>
        </v-btn>
      </div>
    </v-app-bar>

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
    sections: [
      {
        title: "About",
        icon: "mdi mdi-book-open-page-variant",
        link: "#About",
      },
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
</style>
