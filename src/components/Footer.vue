<template>
  <div id="Footer">
    <v-card class="footer" tile>
      <div class="subtitle-2">
        Copyright &copy; 2019 - {{ new Date().getFullYear() }} Holger Mueller |
        <a class="link" href="https://github.com/Holgermueller/portfolio"
          >Repo</a
        >
      </div>
      <div class="caption">This site built with Vue | Vuetify</div>
      <div class="caption">Deployed on Github Pages</div>
    </v-card>
  </div>
</template>

<style scoped>
#Footer {
  position: absolute;
  bottom: 0;
  width: 100%;
}
.footer {
  background-color: #31708e !important;
  color: white;
  padding: 4px;
  text-align: center;
}
.link {
  text-decoration: none;
  color: white;
}
.caption {
  color: white;
}
</style>
