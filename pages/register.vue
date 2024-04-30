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
          <!-- Formulario de registro -->
          <v-card class="mx-auto" max-width="500">
            <v-card-title class="text-center">
              <h1 class="text-xl font-bold leading-tight tracking-tight">
                Crear una Cuenta
              </h1>
            </v-card-title>
            <v-card-text>
              <form @submit.prevent="submitRegister">
                <v-text-field
                  v-model="registerForm.name"
                  label="Nombre"
                  required
                ></v-text-field>
                <v-text-field
                  v-model="registerForm.email"
                  label="Correo"
                  type="email"
                  required
                ></v-text-field>
                <v-text-field
                  v-model="registerForm.password"
                  label="Contraseña"
                  type="password"
                  required
                ></v-text-field>
                <v-text-field
                  v-model="registerForm.confirmPassword"
                  label="Confirmar contraseña"
                  type="password"
                  required
                ></v-text-field>
                <v-checkbox
                  v-model="termsAccepted"
                  label="I accept the Terms and Conditions"
                  required
                ></v-checkbox>
                <v-btn type="submit" color="primary" block>Crear cuenta</v-btn>
              </form>
            </v-card-text>
            <v-card-actions class="justify-center">
              <span class="text-sm font-light"
                >Ya tienes una cuenta?
                <a
                  href="/login"
                  class="font-medium text-primary-600 hover:underline"
                  >Inicia Sesión</a
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
          src: 'register.avif',
          heading: ' Registro ',
        },
      ],
      registerForm: {
        name: '',
        email: '',
        password: '',
        confirmPassword: '',
      },
      termsAccepted: false,
    }
  },
  methods: {
    submitRegister() {
      // Aquí puedes implementar la lógica para enviar los datos del formulario de registro al servidor
    },
  },
}
</script>

<style scoped>
/* Aquí puedes agregar estilos personalizados según sea necesario */
</style>
