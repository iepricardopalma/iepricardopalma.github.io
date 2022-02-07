<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      app
      temporary
      dark
      src="@/assets/img/languagesPosterDark.png">
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <img src="@/assets/img/yobilingue_logo2.jpg" alt="Logo" />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title class="title">YoBilingue</v-list-item-title>
            <v-list-item-subtitle>Idiomas sin barreras</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider />

      <v-list dense>
        <v-list-item
          v-for="([icon, text, link], i) in items"
          :key="i"
          link
          @click="$vuetify.goTo(link)">
          <v-list-item-icon class="justify-center mr-4">
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title style="font-size: 1 rem">
              {{ text }}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      :color="color"
      :flat="flat"
      class="px-15"
      :class="{ expand: flat }">
      <v-toolbar-title>
        <v-img src="@/assets/img/rp_membrete.png" max-width="196px" />
      </v-toolbar-title>
      <v-spacer />
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
        class="mr-2"
        v-if="isXs"/>
      <div v-else>
        <v-btn text @click="$vuetify.goTo('#hero')">
          <span class="mr-2">Inicio</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#features')">
          <span class="mr-2">Nosotros</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#languages')">
          <span class="mr-2">Idiomas</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#workshop')">
          <span class="mr-2">Talleres</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#contact')">
          <span class="mr-2">Testimonios</span>
        </v-btn>
      </div>
    </v-app-bar>
  </div>
</template>

<style lang="scss" scoped>
.v-toolbar {
  transition: 0.6s;
  .v-btn {
    color: #2e3192;
  }
}
.expand {
  height: 80px !important;
  padding-top: 10px;
}
</style>

<script>
export default {
  data: () => ({
    drawer: null,
    isXs: false,
    items: [
      ["mdi-home-outline", "Inicio", "#hero"],
      ["mdi-information-outline", "Nosotros", "#features"],
      ["mdi-book", "Idiomas", "#languages"],
      ["mdi-play", "Talleres", "#workshop"],
      ["mdi-earth", "Testimonios", "#contact"],
    ],
  }),
  props: {
    color: String,
    flat: Boolean,
  },
  methods: {
    onResize() {
      this.isXs = window.innerWidth < 850;
    },
  },

  watch: {
    isXs(value) {
      if (!value) {
        if (this.drawer) {
          this.drawer = false;
        }
      }
    },
  },
  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize, { passive: true });
  },
};
</script>
