<template>
  <section id="intro" class="py-16">
    <v-container>
      <v-responsive class="max-auto mx-auto text-center" max-width="600">
        <v-avatar color="primary" size="70" class="mb-8">
          <v-icon x-large dark>mdi-chart-bubble</v-icon>
        </v-avatar>
        <h2 class="text-h4 text-md-h3 text-center font-weight-black mb-7">
          Empoderando la Salud Mental: Un Viaje Hacia el Bienestar
        </h2>
        <p class="title font-weight-light">
          <strong>MindHarmony</strong> — Descubre Herramientas Innovadoras para
          Combatir la Depresión, Trastornos Alimenticios y Más
        </p>
      </v-responsive>

      <v-row class="pt-12">
        <v-col v-for="card in cards" :key="card.title" cols="12" md="4">
          <v-row no-gutters>
            <v-col :cols="card.callout ? 9 : 12">
              <div class="pr-2">
                <div class="text--disabled" v-text="card.subtitle"></div>
                <h4
                  class="text-uppercase mt-1 mb-4"
                  style="letter-spacing: 0.15em"
                  v-text="card.title"
                ></h4>
                <p v-text="card.text"></p>
              </div>
            </v-col>
            <v-col v-if="card.callout" cols="2">
              <span
                class="text-h3 grey--text font-weight-bold pr-8"
                style="opacity: 0.1"
                >{{ card.callout }}</span
              >
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: 'Depresión',
          subtitle: 'Importancia',
          text: 'La terapia, la medicación y otras formas de tratamiento pueden brindar alivio y ayudarte a encontrar una mayor estabilidad emocional.',
          callout: '01',
        },
        {
          title: 'Problemas alimenticios',
          subtitle: 'Alimentación',
          text: 'Los problemas alimenticios, como la anorexia, la bulimia y el trastorno por atracón, pueden tener un impacto devastador en la vida de quienes los padecen.',
          callout: '02',
        },
        {
          title: 'Importancia de tratarse',
          subtitle: 'Necesario',
          text: 'Tratar la depresión y los problemas alimenticios es fundamental para recuperar el control sobre tu vida y tu bienestar. Ignorar estos problemas o intentar enfrentarlos solo puede llevar a un deterioro continuo de la salud física y mental.',
          callout: '03',
        },
      ],
    }
  },
}
</script>
