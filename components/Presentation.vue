<template>
  <!-- On inverse la logique car les breakpoint ne s'initialisent pas assez tôt -->
  <v-theme-provider dark>
    <div
      class="main-container d-flex flex-column"
      :class="{ mobile: !$vuetify.breakpoint.mdAndUp }"
    >
      <v-row>
        <div>
          <h1>
            {{ page.nom }}
          </h1>
          <nuxt-content :document="page" />
        </div>
      </v-row>
      <!-- TODO Refaire la layout pour rendre le contenu plus lisible -->
      <v-row align="end">
        <scroll-arrow height="80" />
        <v-btn :href="page.url_cv" class="ml-auto">Voir mon CV</v-btn>
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
</style>