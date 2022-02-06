<template>
  <section id="about">
    <v-container fluid class="mt-10 py-10">
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
              <h1 class="font-weight-light display-2 mb-10">¿Quiénes somos?</h1>
              <v-row>
                <v-col cols="12" class="d-flex align-center">
                  <h1 class="font-weight-light display-1">Liderado por becarios</h1>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-icon class="mr-5 about-icon d-none d-sm-flex">mdi-school-outline</v-icon>
                  <p class="font-weight-light text-justify">
                    Somos parte de la Red de becarios del programa educativo Supérate Lima de la Municipalidad de Lima. <br>
                    Compartimos todos nuestros conocimientos adquiridos en idiomas a través de talleres interactivos.
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <h1 class="font-weight-light display-1">Generamos curiosidad y amor por los idiomas</h1>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-icon class="mr-5 about-icon d-none d-sm-flex">mdi-head-heart-outline</v-icon>
                  <p class="font-weight-light text-justify">
                    Queremos generar motivación por el aprendizaje de idiomas y aprendas más sobre los que ya conoces. <br>
                    Buscamos que te identifiques con la cultura de diversos países.
                  </p>
                </v-col>
              </v-row>
            </v-col>
            <v-col cols="12" md="5" class="d-none d-md-flex">
              <v-img
                src="@/assets/img/about1.jpg"
                class="d-block ml-auto mr-auto"
                max-width="400px"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style lang="scss" scoped>
.col {
  p {
    font-size: 1.35rem;
  }
}
.about-icon {
  font-size: 112px;
  margin-bottom: 1.2rem;
  color: rgb(7, 62, 103);
}
</style>
