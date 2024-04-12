<template>
  <section :class="$vuetify.theme.dark ? 'black' : 'white'" class="py-16">
    <v-container>
      <v-row>
        <v-col>
          <v-row no-gutters>
            <v-col class="text-center">
              <h2
                class="text-h4 text-md-h3 text-center font-weight-black text-capitalize mb-4"
              >
                La Mejor Tarifa al Alcance de Todos
              </h2>

              <p class="my-10 title">
                "Accede a servicios de calidad a precios accesibles, diseñados
                para que todos puedan cuidar su bienestar mental sin comprometer
                su bolsillo."
              </p>
              <div class="text-center">
                <v-btn-toggle
                  v-model="planDuration"
                  active-class="primary darken-1"
                  borderless
                  mandatory
                  light
                  color="white"
                >
                  <v-btn value="monthly"> Plan Mensual </v-btn>
                  <v-btn value="yearly"> Plan Anual </v-btn>
                </v-btn-toggle>
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid>
      <v-row class="mx-auto" style="max-width: 1200px">
        <v-col v-for="(plan, ix) in plans" :key="`plan-${ix}`" cols="12" md="4">
          <v-hover v-slot="{ hover }">
            <v-card
              :elevation="hover ? 24 : plan.elevation"
              :color="plan.color"
              max-width="400"
              :class="hover ? 'zoom' : 'notzoom'"
              class="mx-auto transition-swing"
            >
              <h3
                class="text-h4 text-center font-weight-black white--text pt-5"
                v-text="plan.plan"
              ></h3>
              <v-card-text
                class="text-center subtitle-1 white--text py-2"
                v-text="plan.description"
              ></v-card-text>
              <v-card-subtitle
                class="text-h5 font-weight-black text-center white--text pt-0"
                >{{ planDuration === 'monthly' ? plan.monthly : plan.yearly }}
                <span class="subtitle-1"
                  >per {{ planDuration === 'monthly' ? 'month' : 'year' }}</span
                ></v-card-subtitle
              >
              <v-list>
                <v-list-item
                  v-for="(feature, ik) in plan.features"
                  :key="`feature-${ik}`"
                  dense
                >
                  <v-list-item-icon>
                    <v-icon>
                      {{ feature.icon }}
                    </v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title
                      class="text-capitalize"
                      v-text="feature.text"
                    ></v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item>
                  <v-btn
                    color="primary"
                    large
                    block
                    rounded
                    class="mx-auto my-3"
                  >
                    Adquirir Ahora
                  </v-btn>
                </v-list-item>
              </v-list>
            </v-card></v-hover
          >
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      planDuration: 'monthly',
      plans: [
        {
          plan: 'Bienestar Básico',
          elevation: 0,
          color: 'primary darken-1',
          description: 'Plan Óptimo de Bienestar para el Crecimiento Personal',
          monthly: '$10',
          yearly: '$100',
          features: [
            {
              icon: 'mdi-account-heart',
              text: 'Acceso ilimitado a la biblioteca de recursos y artículos sobre salud mental y bienestar',
            },
            {
              icon: 'mdi-chat',
              text: 'Chat en línea con un experto una vez al mes para consultas y orientación',
            },
            {
              icon: 'mdi-brain',
              text: 'Ejercicios de mindfulness y técnicas de relajación personalizadas',
            },
            {
              icon: 'mdi-notebook',
              text: 'Seguimiento del progreso del usuario a través de un diario de emociones y hábitos',
            },
          ],
        },
        {
          plan: 'Salud Mental Intermedio',
          elevation: 16,
          color: 'green darken-2',
          description: 'Paquete Integral de Salud Mental para Individuos',
          monthly: '$40',
          yearly: '$400',
          features: [
            {
              icon: 'mdi-account-heart',
              text: 'Todos los beneficios del Plan Bienestar Básico',
            },
            {
              icon: 'mdi-chat',
              text: 'Chat en línea con un experto dos veces al mes para sesiones de apoyo y orientación personalizada',
            },
            {
              icon: 'mdi-brain',
              text: 'Ejercicios de terapia cognitivo-conductual (TCC) adaptados a las necesidades individuales del usuario',
            },
            {
              icon: 'mdi-notebook',
              text: 'Seguimiento del progreso del usuario a través de evaluaciones regulares de bienestar emocional y mental',
            },
          ],
        },
        {
          plan: 'Empoderamiento Avanzado',
          elevation: 0,
          color: 'orange darken-3',
          description:
            'Programa de Fortalecimiento Mental para el Bienestar Integral',
          monthly: '$100',
          yearly: '$1000',
          features: [
            {
              icon: 'mdi-account-heart',
              text: 'Todos los beneficios del Plan Salud Mental Intermedio',
            },
            {
              icon: 'mdi-chat',
              text: 'Chat en línea ilimitado con un equipo de expertos en salud mental y terapeutas certificados',
            },
            {
              icon: 'mdi-brain',
              text: 'Sesiones de terapia en línea semanales con un terapeuta asignado',
            },
            {
              icon: 'mdi-notebook',
              text: 'Seguimiento del progreso del usuario a través de un plan de tratamiento personalizado y sesiones de revisión mensuales con el terapeuta asignado',
            },
          ],
        },
      ],
    }
  },
}
</script>

<style scoped>
.zoom {
  transform: scale(1.025) translate(0, -10px);
  transition: transform 0.2s;
}
.notzoom {
  transition: transform 0.2s;
}
</style>
