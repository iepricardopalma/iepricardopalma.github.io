<template>
  <section id="workshop">
    <v-container fluid class="workshop">
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col sm="4" class="hidden-xs-only">
              <v-img src="@/assets/img/ill2.svg" class="d-block ml-auto mr-auto" max-width="350px" />
            </v-col>
            <v-col cols="12" sm="8" class="white--text text-left">
              <h1 class="font-weight-light display-1 text-center my-6">
                Desarrollamos talleres semanales. <br>
                 Conocerás expresiones útiles, cultura y oportunidades de estudio.
              </h1>
              <p class="font-weight-light text-justify">
                <v-list>
                  <v-list-item>
                    <v-list-item-icon>
                      <v-icon color="white">mdi-chevron-right</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                      Tendrás acceso a material académico, videos y <b>contenido exclusivo</b> en cada idioma,
                      todo ello a través de la plataforma educativa <a href="https://new.edmodo.com/">Edmodo</a>. </v-list-content>
                    </v-list-item-content>
                  </v-list-item>
                  <v-list-item>
                    <v-list-item-icon>
                      <v-icon color="white">mdi-chevron-right</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                      Nuestros talleres se transmitirán en vivo cada <b>sábado</b>  vía Zoom 
                      y a través del canal de Youtube <a href="https://www.youtube.com/c/LimaEducaci%C3%B3nyDeportes">Lima Educación y Deportes</a>.
                      <strong>(Atentos al anuncio de nuestra próxima edición)</strong> <br>
                      Grupo 1: &nbsp 5 p.m. a 6 p.m. <br>
                      Grupo 2: &nbsp 7 p.m. a 8 p.m. <br>
                    </v-list-item-content>
                  </v-list-item>
                  <v-list-item>
                    <v-list-item-icon>
                      <v-icon color="white">mdi-chevron-right</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                      Los participantes que concluyan las actividades asignadas satisfactoriamente recibirán
                      una <b>certificado de participación</b> a nombre de la Municipalidad de Lima.
                    </v-list-item-content>
                  </v-list-item>
                </v-list>
              </p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style lang="scss" scoped>
#workshop {
  .workshop{
    background-image: url("~@/assets/img/languagesPosterDark.png");
    background-attachment: fixed;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    padding: 64px 0;
    &:before{
      content:'';
      position: absolute;
      top: 0;
	    bottom: 0;
	    left: 0;
	    right: 0;
	    background-color: rgba(0,0,0,0.5);
    }
  }
}
#workshop .container,
#workshop .row {
  height: 100%;
}
.display-1{
  opacity: 0.99;
}
.v-list{
  background-color: transparent;
  .v-list-item{
    align-items: initial;
    .v-list-item__icon{
      margin-right: 12px;
    }
    .v-list-item__content {
      display: block;
      color: white;
    }
  }
}
a{
  font-weight: 500;
  transition: 0.5s ease-out;
  &:hover{
    color: #073E67;
    transition: 0.5s;
  }
}
p, li{
  font-size: 1.35rem;
  margin: 0;
}
</style>
