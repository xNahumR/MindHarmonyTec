<template>
  <section>
    <v-row no-gutters>
      <v-col cols="12">
        <SectionsHeroAlt :hero-alt="heroAlt" />
      </v-col>
    </v-row>
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="6">
          <!-- Formulario de inicio de sesión -->
          <v-card class="mx-auto" max-width="500">
            <v-card-title class="text-center">
              <h1 class="text-xl font-bold leading-tight tracking-tight">
                Inicia Sesión en tu Cuenta
              </h1>
            </v-card-title>
            <v-card-text>
              <form @submit.prevent="submitLogin">
                <v-text-field
                  v-model="loginForm.email"
                  label="Correo email"
                  type="email"
                  required
                ></v-text-field>
                <v-text-field
                  v-model="loginForm.password"
                  label="Contraseña"
                  type="password"
                  required
                ></v-text-field>
                <v-btn type="submit" color="primary" block
                  >Iniciar Sesión</v-btn
                >
              </form>
            </v-card-text>
            <v-card-actions class="justify-center">
              <span class="text-sm font-light"
                >No tienes una cuenta?
                <a
                  href="/register"
                  class="font-medium text-primary-600 hover:underline"
                  >Registrate aquí</a
                ></span
              >
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      heroAlt: [
        {
          src: 'login.avif',
          heading: ' Iniciar Sesión ',
        },
      ],
      head() {
        return {
          title: 'Login',
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
      loginForm: {
        email: '',
        password: '',
      },
    }
  },
  methods: {
    submitLogin() {
      // Aquí puedes implementar la lógica para enviar los datos del formulario de inicio de sesión al servidor
    },
  },
}
</script>

<style scoped>
/* Aquí puedes agregar estilos personalizados según sea necesario */
</style>
