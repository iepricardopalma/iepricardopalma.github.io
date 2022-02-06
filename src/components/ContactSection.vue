<template>
  <section id="contact">
    <v-container fluid class="pa-0">
      <v-carousel
        hide-delimiters
        cycle
        interval="10000">
        <template v-slot:prev="{ on, attrs }">
          <v-btn
            v-bind="attrs"
            v-on="on"
            text
            icon>
            <v-icon x-large>mdi-chevron-left</v-icon>
          </v-btn>
        </template>
        <template v-slot:next="{ on, attrs }">
          <v-btn
            v-bind="attrs"
            v-on="on"
            text
            icon>
            <v-icon>mdi-chevron-right</v-icon>
          </v-btn>
        </template>
        <v-carousel-item
          v-for="(item,i) in testimonials"
          :key="i">
          <v-sheet
            height="100%"
            tile>
            <v-row class="fill-height" align="center" justify="space-around">
              <v-col
              cols="12"
              sm="6"
              class="text-center">
                <v-card
                  elevation="0"
                  color="transparent"
                  class="card">
                  <v-img
                    :src="item.img"
                    contain
                    max-height="148px"
                    class="d-block ml-auto mr-auto"></v-img>
                  <h1 class="font-weight-bold mb-5">{{ item.title }}</h1>
                  <p class="font-weight-regular">
                    {{ item.text }}
                  </p>
                </v-card>
              </v-col>
            </v-row>
          </v-sheet>
        </v-carousel-item>
      </v-carousel>
    </v-container>
    <div class="svg-border-waves text-white">
      <v-img src="~@/assets/img/borderWavesBlue.svg"/>
    </div>
  </section>
</template>

<style lang="scss" scoped>
#contact {
  background-color: #f4f7f5;
  p{
    font-size: 1.25rem;
  }
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: -4px;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}

</style>

<script>

export default {
  data() {
    return {
      testimonials: [
        {
          img: require("@/assets/img/languages/china.svg"),
          title: "María Gracia Rojas Pariona",
          text: "¡Excelente trabajo! Todo el material, las asesorías adicionales, las clases brindadas y cada post publicado en Edmodo han sido de muchísima ayuda. Ha sido un gusto enorme haber conocido más de estos bellos idiomas a los que, sinceramente, antes temía por lo complejo que los percibía. ¡Un abrazo enorme a cada uno de los profes y gracias por todo!",
        },
        {
          img: require("@/assets/img/languages/united-kingdom.svg"),
          title: "Nicole Santos Mesones",
          text: "!Me encantaron los talleres! Gracias por todo el material brindado y gracias por los exámenes de práctica, ya que me ayudaron mucho a reforzar los temas de las semanas <3",
        },
        {
          img: require("@/assets/img/languages/brazil.svg"),
          title: "Yameli Casas Montalvo",
          text: "Quiero agradecer a los profesores y a YO BILINGUE por enseñarnos estos bonitos idiomas, donde aprendí a cómo presentarme y como poder establecer conversaciones. Bendiciones.",
        },
        ]
    }
  }
};
</script>
