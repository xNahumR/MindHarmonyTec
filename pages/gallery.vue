<template>
  <section>
    <v-row no-gutters>
      <v-col cols="12">
        <SectionsHeroAlt :hero-alt="heroAlt" />
        <br />
        <v-card class="mx-auto" max-width="500">
          <v-img class="grey lighten-2 rounded-lg" aspect-ratio="1">
            <video controls width="100%" height="100%" preload="metadata">
              <source
                src="https://www.youtube.com/watch?v=nrpLlOfVY0s"
                type="video/mp4"
              />
              Tu navegador no admite el elemento de video.
            </video>
            <template v-slot:placeholder>
              <v-row class="fill-height ma-0" align="center" justify="center">
                <v-progress-circular
                  indeterminate
                  color="grey lighten-5"
                ></v-progress-circular>
              </v-row>
            </template>
          </v-img>
          <v-card-title class="headline"
            >Autocuidado y Salud Mental</v-card-title
          >
          <v-card-text>
            <p>Atención Personal</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </section>
</template>

<script>
export default {
  data() {
    return {
      heroAlt: [
        {
          src: 'pexels-andrea-piacquadio-3830745.jpg',
          heading: ' Videos ',
        },
      ],
    }
  },
  head() {
    return {
      title: 'Gallery',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            'Infographic hypotheses influencer user experience Long madel ture gen-z paradigm shift client partner network product seilans solve management influencer analytics leverage virality. incubator seed round massmarket. buyer agile development growth hacking business-to-consumer ecosystem',
        },
      ],
    }
  },
}
</script>
