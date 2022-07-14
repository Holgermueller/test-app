<template>
  <div id="connect">
    <h1 class="section-header">Connect</h1>

    <v-card class="connections-display">
      <v-container>
        <v-row>
          <v-col v-for="(connection, index) in connections" :key="index">
            <v-btn
              :href="connection.link"
              target="_blank"
              class="social-link"
              text
              block
            >
              <v-icon> {{ connection.connection_class }}</v-icon>
              <span class="connection-name">{{ connection.name }}</span>
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      connections: [
        {
          name: "Github",
          connection_class: "mdi mdi-github",
          link: "https://github.com/Holgermueller",
        },
        {
          name: "LinkedIn",
          connection_class: "mdi mdi-linkedin",
          link: "https://www.linkedin.com/in/holger-mueller-75855114a/",
        },
      ],
    };
  },
};
</script>

<style scoped>
.section-header {
  text-align: center;
  margin-top: 7%;
}
</style>
