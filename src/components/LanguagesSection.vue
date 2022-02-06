<template>
  <v-container fluid id="languages" class="mt-8   py-8">
    <v-row align="center" justify="center">
      <v-col cols="12">
        <h1 class="font-weight-light text-center display-2 mb-4">¿Qué idiomas aprenderás?</h1>
      </v-col>
      <v-col cols="10" class="py-8">
        <v-row align="center" justify="space-around">
          <v-col
            cols="12"
            sm="4"
            class="text-center"
            v-for="(feature, i) in features"
            :key="i"
          >
            <v-hover v-slot:default="{ hover }">
              <v-card
                class="card"
                color="transparent"
                :elevation="hover ? 0 : 0"
                :class="{ up: hover }"
              >
                <v-img
                  :src="feature.img"
                  max-width="140px"
                  class="d-block ml-auto mr-auto"
                  :class="{ 'zoom-efect': hover }"
                ></v-img>
                <h1 class="font-weight-regular">{{ feature.title }}</h1>
                <!--h4 class="font-weight-regular subtitle-1">
                  {{ feature.text }}
                </h4-->
              </v-card>
            </v-hover>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="12">
        <p class="font-weight-light text-center display-1">Aquí un poco más sobre <a href="https://youtube.com/playlist?list=PLhJHiRCP94SU9wzxPWSnxlNeaBHshx8jA">nuestros talleres</a>.</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<style lang="scss">
.card {
  min-height: 200px;
  padding: 10px;
  transition: .4s ease-out;
}

.card {
  h1{
    margin: auto;
    width: max-content;
  }
  .v-image {
    margin-bottom: 15px;
    transition: 0.75s;
  }
}

.zoom-efect {
  transform: scale(1.1);
}

.up {
  transform: translateY(-12px);
  transition: 0.5s ease-out;
}
</style>

<script>
export default {
  data () {
    return {
      features: [
        {
          img: require("@/assets/img/languages/united-kingdom.svg"),
          title: "Inglés",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          img: require("@/assets/img/languages/italy.svg"),
          title: "Italiano",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          img: require("@/assets/img/languages/brazil.svg"),
          title: "Portugués",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          img: require("@/assets/img/languages/germany.svg"),
          title: "Alemán",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          img: require("@/assets/img/languages/china.svg"),
          title: "Chino mandarín",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          img: require("@/assets/img/languages/indonesia.svg"),
          title: "Indonesio",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
      ],
    }
  }
}
</script>
