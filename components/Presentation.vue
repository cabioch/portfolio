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
    <v-row align-content="end" justify="end">
      <v-btn :href="page.url_cv">Voir mon CV</v-btn>
    </v-row>
  </div>
</template>

<script>
import ButtonSource from './ButtonSource.vue'
export default {
  components: { ButtonSource },
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