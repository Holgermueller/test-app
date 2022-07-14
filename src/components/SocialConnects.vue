<template>
  <div id="socialConnects">
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
  name: "SocialConnects",

  data: () => ({
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
  }),
};
</script>

<style scoped>
.connections-display {
  width: 75%;
  margin-top: 2rem;
  margin-left: auto;
  margin-right: auto;
  background-color: #f7f9fb;
}
.social-link:hover {
  color: #31708e;
}
</style>
