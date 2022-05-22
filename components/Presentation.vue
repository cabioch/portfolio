<template>
  <!-- On inverse la logique car les breakpoint ne s'initialisent pas assez tôt -->
  <v-theme-provider dark>
    <div class="main-container d-flex flex-column" :class="{ mobile: !$vuetify.breakpoint.mdAndUp }">
      <v-row>
        <div>
          <h1 class="text-h1">
            Bienvenue sur mon portfolio
          </h1>
          <div :class="{ description: $vuetify.breakpoint.mdAndUp }">
            <h6 class="text-h6">
              <nuxt-content :document="page" />
            </h6>
          </div>
        </div>
      </v-row>
      <!-- TODO Refaire la layout pour rendre le contenu plus lisible -->
      <v-row align="end" justify="end">
        <v-col>
          <scroll-arrow height="80" />
        </v-col>
        <div class="button-group">
          <v-btn href="https://www.linkedin.com/in/enzo-cabioch-b62759229/">
            <v-icon left>mdi-linkedin</v-icon>Mon profil LinkedIn
          </v-btn>
          <v-btn href="/tableau_synthese.pdf">Voir mon tableau de compétences</v-btn>
          <v-btn :href="page.url_cv">Voir mon CV</v-btn>
        </div>
      </v-row>
    </div>
  </v-theme-provider>
</template>

<script>
export default {
  props: {
    page: {
      required: true,
    },
  },
}
</script>

<style scoped>
.main-container {
  padding: 10% 5% 5%;
  height: 100%;
  background-image: url('~/static/img_nobright.jpg');
  background-position: center;
  background-size: cover;
  color: white;
}

.mobile {
  /* TODO Travailler l'UI mobile */
  padding-bottom: 20%;
}

.description {
  max-width: 70%;
}

.button-group>* {
  margin: 0 1em;
}
</style>