<template>
  <section id="hero">
    <v-carousel
      height="calc(100vh - 64px)"
      dark
      cycle
      show-arrows-on-hover
      draggable="true"
      hide-delimiter-background
    >
      <v-carousel-item
        v-for="(carousel, carindex) in carouselsData"
        :key="carindex"
        :src="carousel.src"
        class="gradient-fill"
      >
        <v-container fill-height>
          <div style="max-width: 600px">
            <div
              class="text-md-h2 mb-3 text-sm-h3 text-h5 font-weight-black white--text"
            >
              {{ carousel.heading.toUpperCase() }}
            </div>
            <p class="mb-5 white--text">{{ carousel.subHeading }}</p>
            <v-btn :x-large="$vuetify.breakpoint.smAndUp" class="my-3 primary"
              >EMPIEZA EL CAMBIO</v-btn
            >
            <span class="mx-2 my-4"></span>
            <v-btn
              :x-large="$vuetify.breakpoint.smAndUp"
              text
              class="my-3"
              outlined
              dark
              ><v-icon left large color="primary">mdi-play</v-icon>DESCUBRE
              MÁS</v-btn
            >
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
      carouselsData: [
        {
          src: 'pexels-andrea-piacquadio-3884440.jpg',
          heading: ' MEJORA TU SALUD ',
          subHeading:
            ' Desata el poder de tu mente priorizando tu salud mental. En un mundo acelerado lleno de cambios constantes y normas en evolución, proteger tu bienestar mental es de suma importancia. Sumérgete en nuestra amplia gama de recursos de salud mental diseñados para nutrir tu viaje hacia el bienestar cognitivo.',
        },
        {
          src: 'pexels-peter-olexa-4012966.jpg',
          heading: ' LA NUTRICIÓN ES LA CLAVE ',
          subHeading:
            ' Comer bien es fundamental para nuestra salud y bienestar general. Proporciona a nuestros cuerpos los nutrientes necesarios para funcionar de manera óptima y apoya diversos procesos corporales. Una dieta equilibrada, rica en frutas, verduras, granos integrales, proteínas magras y grasas saludables, no solo alimenta nuestras actividades físicas, sino que también nutre nuestras mentes. ',
        },
        {
          src: 'pexels-thirdman-5961072.jpg',
          heading: ' ESCPECIALISTAS ',
          subHeading:
            ' Así como consultarías a un médico para dolencias físicas, es igualmente importante buscar ayuda profesional cuando enfrentas dificultades emocionales o psicológicas. Los profesionales de la salud mental, como terapeutas, consejeros y psicólogos, están equipados con el conocimiento y las habilidades para brindar apoyo y tratamientos personalizados para abordar una amplia gama de preocupaciones de salud mental. ',
        },
        {
          src: 'pexels-andrea-piacquadio-3830745.jpg',
          heading: ' IMPROVE YOUR MOOD ',
          subHeading:
            ' Improving mood is an essential aspect of maintaining overall well-being and enjoying life to the fullest. While mood fluctuations are a natural part of the human experience, there are several strategies you can employ to enhance your mood and cultivate a greater sense of happiness and fulfillment. ',
        },
      ],
    }
  },
}
</script>

<style>
.gradient-fill .v-responsive__content {
  background: rgb(0, 0, 0);
  background: linear-gradient(
    to right,
    rgba(3, 12, 41, 0.75),
    rgba(5, 11, 31, 0.65)
  );
}
</style>
