<template>
  <div class="main-container d-flex flex-column">
    <v-row>
      <div>
        <h1>
          {{ page.nom }}
        </h1>
        <nuxt-content :document="page" />
      </div>
    </v-row>
    <!-- TODO Refaire la layout -->
    <v-row align="end">
      <scroll-arrow height="80" />
      <v-btn :href="page.url_cv" class="ml-auto">Voir mon CV</v-btn>
    </v-row>
  </div>
</template>

<script>
import ButtonSource from './ButtonSource.vue'
import ScrollArrow from './ScrollArrow.vue'
export default {
  components: { ButtonSource, ScrollArrow },
  props: {
    page: {
      required: true,
    },
  },
}
</script>

<style scoped>
.main-container {
  padding: 5%;
  height: 100%;
}
</style>