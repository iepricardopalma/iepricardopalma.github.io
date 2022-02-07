<template>
  <v-app>
    <navigation :color="color" :flat="flat" />
    <v-main class="pt-0">
      <home />
      <about />
      <languages/>
      <workshop />
      <contact />
    </v-main>
    <v-scale-transition>
      <v-btn
        fab
        v-show="fab"
        v-scroll="onScroll"
        dark
        fixed
        bottom
        right
        color="secondary"
        @click="toTop"
      >
        <v-icon>mdi-arrow-up</v-icon>
      </v-btn>
    </v-scale-transition>
    <foote />
  </v-app>
</template>

<style scoped>
/**
COLORES RICARDO PALMA

AZUL
#2e3192
rgb(46, 49, 146)

ROJO
#e71e23
rgb(231,30,35)

DORADO
#BC9C22
rgb(180, 154, 54)
**/

.v-main {
  background-image: url("~@/assets/img/bgMain.png");
  background-attachment: fixed;
  background-position: center;
  background-size: cover;
}
</style>

<script>
import navigation from "./components/Navigation";
import home from "./components/HomeSection";
import about from "./components/AboutSection";
import languages from "./components/LanguagesSection";
import workshop from "./components/WorkshopSection";
import contact from "./components/ContactSection";
import foote from "./components/Footer";

export default {
  name: "App",

  components: {
    navigation,
    home,
    about,
    languages,
    workshop,
    contact,
    foote,
  },

  data: () => ({
    fab: null,
    color: "",
    flat: null,
  }),

  created() {
    const top = window.pageYOffset || 0;
    if (top <= 60) {
      this.color = "transparent";
      this.flat = true;
    }
  },

  watch: {
    fab(value) {
      if (value) {
        this.color = "#ffffff";
        this.flat = false;
      } else {
        this.color = "transparent";
        this.flat = true;
      }
    },
  },

  methods: {
    onScroll(e) {
      if (typeof window === "undefined") return;
      const top = window.pageYOffset || e.target.scrollTop || 0;
      this.fab = top > 60;
    },
    toTop() {
      this.$vuetify.goTo(0);
    },
  },
};
</script>
