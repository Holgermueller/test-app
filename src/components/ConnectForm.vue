<template>
  <div id="ConnectForm">
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
                class="form-control col-12 message"
                rows="5"
                name="message"
              ></textarea>
            </label>
            <!-- your other form fields go here -->
            <button
              name="submit"
              type="submit"
              class="submit"
              :disabled="Name === '' || Email === '' || Message === ''"
            >
              Send It!
            </button>
          </form>
          <small
            >Form powered by
            <a href="https://formspree.io/" target="_blank">Formspree</a>
          </small>
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "ConnectForm",
  data: () => ({
    Name: "",
    Email: "",
    Message: "",
  }),
};
</script>

<style scoped>
.form-card {
  width: 55%;
  margin: 1rem auto;
  background-color: rgb(49, 112, 142, 0.3);
}
.form-container {
  margin-top: 4rem;
}
.button {
  margin-bottom: 10px;
}
label {
  color: #080808;
}
input[type="text"],
input[type="email"],
textarea {
  background-color: white;
  color: #080808;
  font-size: 1.25rem;
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
.message {
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
  color: #080808;
}
a {
  text-decoration: none;
}
</style>
