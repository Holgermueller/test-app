<template>
  <div id="Banner">
    <v-card tile elevation="0" class="banner-content">
      <v-card-text>
        <v-row align="center" justify="center">
          <v-img
            class="pic"
            src="../images/profile.png"
            alt="Pic_of_Me"
            max-height="300"
            max-width="300"
          ></v-img>
        </v-row>

        <div class="name display-4">Holger Mueller</div>
        <div class="description title">
          UX/UI Designer | Full-stack Developer | JAMstacker
        </div>
      </v-card-text>
      <v-card-actions class="links">
        <div class="social-links" v-for="(link, index) in links" :key="index">
          <v-btn
            :href="link.link"
            target="_blank"
            class="link"
            elevation="0"
            fab
            x-large
          >
            <v-icon>{{ link.icon }}</v-icon>
          </v-btn>
        </div>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "SiteBanner",

  data: () => ({
    links: [
      {
        name: "Github",
        link: "https://github.com/Holgermueller",
        icon: "mdi mdi-github",
      },
      {
        name: "Stack Overflow",
        link: "https://stackoverflow.com/users/9111512/holger-mueller?tab=profile",
        icon: "mdi mdi-stack-overflow",
      },
      {
        name: "LinkedIn",
        link: "https://www.linkedin.com/in/holger-mueller-75855114a/",
        icon: "mdi mdi-linkedin",
      },
      {
        name: "Resume",
        link: "https://holgermueller.github.io/Resume/",
        icon: "mdi mdi-file",
      },
      {
        name: "Email",
        link: "mailto:9jholger@gmail.com",
        icon: "mdi mdi-email",
      },
    ],
  }),
};
</script>

<style scoped>
#Banner {
  z-index: 1;
  width: 100%;
  bottom: 0;
}
.banner-content {
  background-color: #f7f9fb !important;
  text-align: center;
  width: 100%;
}
.pic {
  margin-top: 2rem;
  object-fit: cover;
}
.name {
  padding: 2%;
}
.subheader {
  padding: 1%;
}
.social-links {
  display: flex;
  justify-content: space-between;
  column-gap: 0.5rem;
  flex-wrap: wrap;
}
.links {
  width: max-content;
  margin-left: auto;
  margin-right: auto;
}
.link:hover {
  cursor: pointer;
  color: white;
  background-color: #31708e;
}
.name,
.description,
.link {
  color: #31708e;
  background-color: #f7f9fb;
}
@media (min-width: 360px) and (max-width: 450px) {
  .links {
    width: 50%;
  }
}
</style>
