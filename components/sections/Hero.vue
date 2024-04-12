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
              >Get Started</v-btn
            >
            <span class="mx-2 my-4"></span>
            <v-btn
              :x-large="$vuetify.breakpoint.smAndUp"
              text
              class="my-3"
              outlined
              dark
              ><v-icon left large color="primary">mdi-play</v-icon>Learn
              More</v-btn
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
          heading: ' IMPROVE YOUR HEALTH WITH US ',
          subHeading:
            ' Unleash the power of your mind by prioritizing your mental health. In a fast-paced world filled with constant change and evolving norms, safeguarding your mental well-being is of utmost importance. Dive into our comprehensive array of mental health resources designed to nurture your cognitive wellness journey. ',
        },
        {
          src: 'pexels-peter-olexa-4012966.jpg',
          heading: ' NUTRITION IS KEY ',
          subHeading:
            ' Eating well is fundamental to our overall health and well-being. It provides our bodies with the necessary nutrients to function optimally and supports various bodily processes. A balanced diet rich in fruits, vegetables, whole grains, lean proteins, and healthy fats not only fuels our physical activities but also nourishes our minds. ',
        },
        {
          src: 'pexels-thirdman-5961072.jpg',
          heading: ' SPECIALISTS ',
          subHeading:
            ' Just as you would consult a doctor for physical ailments, its equally important to seek professional help when facing emotional or psychological difficulties. Mental health professionals, such as therapists, counselors, and psychologists, are equipped with the knowledge and skills to provide tailored support and interventions to address a wide range of mental health concerns ',
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
