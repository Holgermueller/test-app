<template>
  <div id="Connect">
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
/* #Connect {
background-color: #8fc1e3;
} */
.section-header {
  text-align: center;
  margin-top: 7%;
}
.connections-display {
  width: 75%;
  margin-top: 2rem;
  margin-left: auto;
  margin-right: auto;
  background-color: #8fc1e3;
}
.social-link:hover {
  color: #31708e;
}
.form-container {
  margin-top: 4rem;
}
.form-header {
  text-align: center;
}
.form {
  width: 55%;
  margin-top: 1rem;
  margin-left: auto;
  margin-right: auto;
}
.button {
  margin-bottom: 10px;
}
.hidden {
  display: none;
}
.form-field {
  width: 100%;
  height: 50px;
  border: 1px solid darkgray;
  border-radius: 15px;
  margin: 8px auto;
  padding-left: 8px;
  z-index: 1;
}
.text-field {
  margin: 8px auto;
  border-radius: 15px;
}
.submit {
  width: 100%;
  height: 50px;
  margin: 8px auto;
  background-color: #31708e;
  color: #f7f9fb;
  font-size: 1rem;
  font-weight: bold;
  border-radius: 15px;
}
.submit:disabled {
  background-color: lightgrey;
}
@media (min-width: 360px) and (max-width: 450px) {
  .connection-name {
    font-size: 0;
  }
  .form-header {
    width: 85%;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
