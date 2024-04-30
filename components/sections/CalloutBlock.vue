<template>
  <section
    :class="
      $vuetify.theme.dark
        ? 'grey darken-4 primary--text text--lighten-1'
        : 'grey lighten-4 primary--text'
    "
    class="primary--text py-16"
  >
    <v-container>
      <v-row>
        <v-col>
          <v-row no-gutters>
            <v-col cols="12" sm="7" class="text-center">
              <h2
                class="text-h4 text-md-h3 text-center font-weight-black text-capitalize mb-4"
              >
                Regístrate aquí
              </h2>

              <p>
                Buscar ayuda es el primer paso hacia la recuperación y el
                bienestar. A través del apoyo adecuado y el tratamiento
                especializado, es posible encontrar alivio y aprender a manejar
                los desafíos que enfrentas.
              </p>
            </v-col>
            <v-col align-self="center" cols="12" sm="5" class="text-center">
              <v-btn
                to="/register"
                x-large
                rounded
                color="white primary--text mx-auto mt-10 px-16"
                >Registro</v-btn
              >
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
