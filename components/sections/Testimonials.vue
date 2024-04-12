<template>
  <section
    id="testimonials"
    :class="$vuetify.theme.dark ? 'black' : 'white'"
    class="py-16"
  >
    <h2 class="text-h4 text-md-h3 text-center font-weight-black mb-8 my-8">
      Testimonios de Usuarios
    </h2>
    <v-carousel
      cycle
      draggable="true"
      hide-delimiter-background
      hide-delimiters
    >
      <v-carousel-item v-for="(item, i) in testimonials" :key="i" class="">
        <v-container fill-height>
          <div style="max-width: 700px" class="mx-auto text-center">
            <v-avatar size="128" class="mb-7">
              <img
                :src="`/team/${item.avtar}`"
                alt="John"
                width="128"
                height="128"
              />
            </v-avatar>
            <h3
              :class="
                $vuetify.theme.dark
                  ? 'black'
                  : 'white grey--text text--darken-2'
              "
              class="mb-1 font-weight-black text-uppercase"
            >
              {{ item.name }}
            </h3>
            <div class="mb-10 font-weight-light grey--text text-uppercase">
              {{ item.post }}
            </div>
            <v-row>
              <v-col cols="1"
                ><v-icon x-large class="grey--text text--lighten-1"
                  >mdi-format-quote-open</v-icon
                ></v-col
              >
              <v-col cols="10">
                <div
                  :class="
                    $vuetify.theme.dark
                      ? 'black'
                      : 'white grey--text text--darken-2'
                  "
                  class="mb-5 font-italic"
                >
                  Descubrir esta página fue un verdadero punto de inflexión en
                  nuestras vidas. Durante años, cada uno de nosotros luchó con
                  desafíos diferentes: la depresión, un trastorno alimenticio,
                  la ansiedad y el dolor de una pérdida. Pero gracias a las
                  herramientas y el apoyo que encontramos aquí, finalmente
                  comenzamos a encontrar nuestro camino hacia la curación y el
                  bienestar.
                </div>
              </v-col>
              <v-col cols="1"
                ><v-icon x-large class="grey--text text--lighten-1"
                  >mdi-format-quote-close</v-icon
                ></v-col
              >
            </v-row>
          </div>
        </v-container>
      </v-carousel-item>
    </v-carousel>
  </section>
</template>

<script>
export default {
  data() {
    return {
      testimonials: [
        {
          avtar: 'person-4.jpg',
          name: 'Mario Speedwagon',
          post: 'Maestro de Escuela',
        },
        {
          avtar: 'person-8.jpg',
          name: 'Petey Cruiser',
          post: 'CEO de Json LLC',
        },
        {
          avtar: 'person-7.jpg',
          name: 'Anna Sthesia',
          post: 'Director de Cleaner LTD',
        },
        {
          avtar: 'person-10.jpg',
          name: 'Paul Molive',
          post: 'Estudiante Universitario',
        },
        {
          avtar: 'person-9.jpg',
          name: 'Gail Forcewind',
          post: 'Recursos Humanos Manager',
        },
      ],
    }
  },
}
</script>
