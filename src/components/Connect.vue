<template>
  <div id="Connect">
    <div class="image">
      <div class="caption">
        <span class="border">CONNECT</span>
      </div>
    </div>

    <div class="connection-section">
      <SocialConnects />

      <ConnectForm />
    </div>
  </div>
</template>

<script>
import SocialConnects from "./SocialConnects.vue";
import ConnectForm from "./ConnectForm.vue";

export default {
  components: {
    SocialConnects,
    ConnectForm,
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
  padding-bottom: 7%;
  margin-bottom: 0;
}
.image {
  /* image by Pixabay via Pexels */
  background-image: url("../images/connect.png");
  background-size: cover;
  height: 500px;
  width: 100%;
}
.caption {
  width: 100%;
  position: relative;
  left: 0;
  top: 50%;
  text-align: center;
  color: black;
}
.caption span.border {
  background-color: white;
  color: black;
  width: fit-content;
  font-size: 25px;
  padding: 18px;
  letter-spacing: 10px;
}
.connection-section {
  margin: 5% auto;
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
