<template>
  <div id="socialConnects">
    <v-card class="connections-display">
      <v-card-title>
        <h2>You can find me on these sites:</h2>
      </v-card-title>
      <v-card-text>
        <hr />
        <v-container>
          <v-row>
            <v-col v-for="(connection, index) in connections" :key="index">
              <v-btn
                :href="connection.link"
                target="_blank"
                class="social-link"
                text
                block
                x-large
              >
                <v-icon> {{ connection.connection_class }}</v-icon>
                <span class="connection-name">{{ connection.name }}</span>
              </v-btn>
            </v-col>
          </v-row>
        </v-container>
      </v-card-text>
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
        attributeName: "social-link",
      },
      {
        name: "Stack Overflow",
        connection_class: "mdi mdi-stack-overflow",
        link: "https://stackoverflow.com/users/9111512/holger-mueller",
        attributeName: "social-link",
      },
      {
        name: "LinkedIn",
        connection_class: "mdi mdi-linkedin",
        link: "https://www.linkedin.com/in/holger-mueller-75855114a/",
        attributeName: "social-link",
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
