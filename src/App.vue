<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <h1>Holger Mueller</h1>
      </div>

      <v-spacer></v-spacer>

      <v-btn text>
        <span class="mr-2">About</span>
      </v-btn>
      <v-btn text>
        <span class="mr-2">Portfolio</span>
      </v-btn>
      <v-btn text>
        <span class="mr-2">Education</span>
      </v-btn>
      <v-btn text>
        <span class="mr-2">Connect</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <Index />
    </v-main>
  </v-app>
</template>

<script>
import Index from "./components/Index.vue";

export default {
  name: "App",

  components: {
    Index,
  },

  data: () => ({
    //
  }),
};
</script>
