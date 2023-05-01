<template>
  <div id="topButton">
    <v-btn
      id="button"
      @click="scrollToTop"
      v-scroll="onScroll"
      v-show="button"
      button
      color="primary"
      title="Back to Top"
      bottom
      right
      fixed
      dark
      fab
    >
      <h1>
        <span class="mdi mdi-chevron-up"></span>
      </h1>
    </v-btn>
  </div>
</template>

<script>
export default {
  data() {
    return {
      button: false,
    };
  },
  methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" });
    },
    onScroll(e) {
      if (typeof window === "undefined") return;
      const top = window.pageYOffset || e.target.scrollToTop || 0;
      this.button = top > 20;
    },
  },
};
</script>
