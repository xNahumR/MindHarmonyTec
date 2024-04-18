<template>
  <section>
    <v-row no-gutters>
      <v-col cols="12">
        <SectionsHeroAlt :hero-alt="heroAlt" />
        <v-container>
          <v-row class="py-16">
            <v-col cols="12">
              <h2
                class="text-h4 text-md-h3 text-center font-weight-black text-capitalize"
              >
                Quiénes Somos?
              </h2>
              <h3
                class="text-h4 text-uppercase font-weight-thin text-center my-8"
              >
                Somos un equipo comprometido con el bienestar mental y emocional
                de nuestros usuarios.
              </h3>
            </v-col>
            <v-col cols="12" md="6">
              <p>
                Nuestra misión es proporcionar un espacio seguro y acogedor
                donde las personas puedan encontrar apoyo, recursos y
                orientación para mejorar su calidad de vida.
              </p>
              <blockquote class="text-h4 pa-5 my-4 font-weight-thin">
                Nuestro sitio web es una plataforma dedicada al bienestar mental
                y emocional.
              </blockquote>
              <p>
                Con un diseño intuitivo y fácil de navegar, nuestro sitio web
                está diseñado para ser accesible para todos. Ya sea que estés
                buscando consejos para manejar el estrés, ejercicios de
                relajación o información sobre terapia, nuestro sitio tiene todo
                lo que necesitas para cuidar tu bienestar emocional.
              </p>
            </v-col>
            <v-col cols="12" md="6">
              <p>
                Nos dedicamos a ofrecer herramientas prácticas, consejos útiles
                y acceso a expertos en salud mental para ayudar a nuestros
                usuarios a cultivar una mente más fuerte y resiliente. Estamos
                aquí para acompañarte en tu viaje hacia una vida más equilibrada
                y satisfactoria.
              </p>
            </v-col>
          </v-row>
        </v-container>
        <SectionsTeam :our-team="ourTeam" />

        <v-row no-gutters>
          <v-col cols="12" md="6" align-self="center">
            <v-img
              max-height="800"
              src="pexels-canva-studio-3277806.jpg"
              lazy-src="pexels-canva-studio-3277806.jpg"
            >
            </v-img>
          </v-col>
          <v-col cols="12" md="6" align-self="center">
            <div class="pa-lg-16 pa-md-10 px-4 py-16">
              <h2 class="text-h3 text-center font-weight-black">
                Nuestra Visión
              </h2>
              <h3
                class="text-h5 text-uppercase font-weight-thin text-center my-8"
              >
                Además, estamos comprometidos con la privacidad y la
                confidencialidad de nuestros usuarios
              </h3>
              <p>
                Nuestra visión es ser un referente en el ámbito del bienestar
                mental en línea, siendo reconocidos por nuestra calidad,
                accesibilidad y compromiso con la salud emocional de nuestros
                usuarios. Nos esforzamos por crear una comunidad en línea donde
                todas las personas se sientan bienvenidas y apoyadas en su
                búsqueda de una vida más equilibrada y satisfactoria.
              </p>
            </div>
          </v-col>
        </v-row>
        <v-row no-gutters class="flex-row-reverse">
          <v-col cols="12" md="6" align-self="center">
            <v-img
              max-height="800"
              src="pexels-rfstudio-3810792.jpg"
              lazy-src="pexels-rfstudio-3810792.jpg"
            >
            </v-img>
          </v-col>
          <v-col cols="12" md="6" align-self="center">
            <div class="pa-lg-16 pa-md-10 px-4 py-16">
              <h2 class="text-h3 text-center font-weight-black">
                Nuestra Misión
              </h2>
              <h3
                class="text-h5 text-uppercase font-weight-thin text-center my-8"
              >
                Asegurando un entorno seguro y acogedor para todos aquellos que
                buscan apoyo en su viaje hacia una vida más equilibrada y
                satisfactoria.
              </h3>
              <p>
                Nuestra misión es proporcionar un espacio seguro y acogedor en
                línea donde las personas puedan acceder a recursos, orientación
                y apoyo para mejorar su salud mental y emocional. Estamos
                comprometidos a ofrecer contenido de calidad, herramientas
                prácticas y acceso a expertos en salud mental para ayudar a
                nuestros usuarios a desarrollar una mente más fuerte y
                resiliente.
              </p>
            </div>
          </v-col>
        </v-row>
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
          src: 'pexels-moose-photos-1036641.jpg',
          heading: ' CONTACTOS ESPECIALISTAS ',
        },
      ],
      ourTeam: [
        {
          name: 'John Churchill',
          position: 'Psicólogo Clínico',
          phone: '+1 (987) 1625346',
          email: 'john@example.com',
          photo: 'person-1.jpg',
        },
        {
          name: 'Fiona	Ross',
          position: 'Nutriologa Clínica',
          phone: '+1 (987) 5894684',
          email: 'fiona@example.com',
          photo: 'person-2.jpg',
        },
        {
          name: 'Justin	Rees',
          position: 'Psiquiatra',
          phone: '+1 (987) 6982456',
          email: 'justin@example.com',
          photo: 'person-3.jpg',
        },
        {
          name: 'Amelia	Ogden',
          position: 'Nutricionista geriátrico',
          phone: '+1 (987) 6982456',
          email: 'amelia@example.com',
          photo: 'person-4.jpg',
        },
        {
          name: 'Sebastian Bailey',
          position: 'Psicólogo del desarrollo',
          phone: '+1 (987) 6982456',
          email: 'sebastian@example.com',
          photo: 'person-5.jpg',
        },
      ],
    }
  },
  head() {
    return {
      title: 'Sobre Nosotros',
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
