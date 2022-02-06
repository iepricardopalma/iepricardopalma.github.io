<template>
  <v-footer dark padless>
    <v-card flat tile class="secondary white--text text-center">
      <v-card-text>
        <p style="font-size: 1.2rem;">Búscanos en nuestras redes sociales</p>
        <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-4 white--text"
          :href="icon.link"
          target="_blank"
          icon
        >
          <v-icon size="36px">{{ icon.text }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text">
        Desarrollado con <strong class="red--text"> &#10084; </strong> por
        <a href="https://jhannrlml.github.io/">
          <strong>Jhann Reyes</strong>
        </a>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Yo Bilingue</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<style lang="scss" scoped>
.v-card {
  width: 100%;
}
a {
  text-decoration: none;
}
</style>

<script>
export default {
  data: () => ({
    icons: [
      {
        text: "mdi-facebook",
        link: "https://www.facebook.com/yobilingue.mun/",
      },
/*      {
        text: "mdi-twitter",
        link: "",
      },
      {
        text: "mdi-linkedin",
        link: "",
      }, */
      {
        text: "mdi-instagram",
        link: "https://www.instagram.com/yobilingue.mun/",
      },
    ],
  }),
};
</script>
