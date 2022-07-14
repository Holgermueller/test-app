<template>
  <div id="Connect">
    <h1 class="section-header">Connect</h1>

    <SocialConnects />

    <div class="form-container">
      <v-card class="form-card">
        <v-card-title>
          <h3>Or drop me a message. I'll respond faster this way.</h3>
        </v-card-title>
        <v-card-text>
          <form
            action="https://formspree.io/f/myyoqqvy"
            method="POST"
            class="form"
          >
            <label
              >Name:
              <input
                v-model="Name"
                type="text"
                name="name"
                class="form-field"
              />
            </label>
            <label>
              Your email:
              <input
                v-model="Email"
                type="email"
                name="email"
                class="form-field"
              />
            </label>
            <label>
              Your message:
              <textarea
                v-model="Message"
                class="form-control col-12"
                rows="5"
                name="message"
              ></textarea>
            </label>
            <!-- your other form fields go here -->
            <button
              type="submit"
              class="submit"
              :disabled="Name === '' || Email === '' || Message === ''"
            >
              Send It!
            </button>
          </form>
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
import SocialConnects from "./SocialConnects.vue";

export default {
  components: {
    SocialConnects,
  },
  data: () => ({
    Name: "",
    Email: "",
    Message: "",
  }),
};
</script>

<style scoped>
#Connect {
  background-color: #8fc1e3;
  padding-top: 4%;
  padding-bottom: 7%;
}
.section-header {
  text-align: center;
  margin-top: 7%;
}
.form-card {
  width: 55%;
  margin-top: 1rem;
  margin-left: auto;
  margin-right: auto;
  background-color: #f7f9fb;
}
.form-container {
  margin-top: 4rem;
}
.button {
  margin-bottom: 10px;
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
  border: 1px solid darkgray;
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
