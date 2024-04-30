<template>
  <section>
    <v-row no-gutters>
      <v-col cols="12">
        <SectionsHeroAlt :hero-alt="heroAlt" />
        <v-container class="py-16">
          <h2
            class="text-h4 text-md-h3 text-center font-weight-black text-capitalize"
          >
            Lo Que Hacemos
          </h2>
          <p class="text-h6 text-uppercase font-weight-light text-center my-16">
            Descubre cómo nuestros servicios personalizados te guían hacia la
            salud mental y emocional que mereces.
          </p>
          <v-row>
            <v-col
              v-for="(card, index) in cards"
              :key="index"
              cols="12"
              sm="6"
              md="4"
              xl="2"
              class="text-center"
            >
              <v-avatar size="80" class="mb-5" color="primary">
                <v-icon dark large>
                  {{ card.icon }}
                </v-icon>
              </v-avatar>
              <div
                class="title text-uppercase mt-1 mb-4"
                v-text="card.title"
              ></div>
              <p v-text="card.text"></p>
              <v-row no-gutters>
                <v-col cols="12"> </v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-container>
        <SectionsPricing />
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
          src: 'pexels-ekaterina-bolovtsova-4048767.jpg',
          heading: ' Servicios ',
        },
      ],
      cards: [
        {
          title: 'Material Design',
          text: 'Explora nuestra plataforma diseñada con Material Design para acceder a herramientas poderosas que promueven la salud mental y el bienestar.',
          icon: 'mdi-material-design',
        },
        {
          title: 'Chat En Línea',
          text: 'Conéctate con nuestros expertos en salud mental a través de nuestro chat en línea y recibe orientación personalizada cuando más lo necesites.',
          icon: 'mdi-message-text-outline',
        },
        {
          title: 'Video y Audio',
          text: 'Sumérgete en una variedad de videos y audios diseñados para promover el bienestar emocional y la resiliencia.',
          icon: 'mdi-eye',
        },
      ],
    }
  },
  head() {
    return {
      title: 'Services',
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
