<template>
  <!-- TODO: Ajouter un tooltip -->
  <v-btn fab :href="url" class="btn-github">
    <v-icon>mdi-github</v-icon>
  </v-btn>
</template>

<script>
export default {
  props: {
    url: String,
  },
}
</script>

<style scoped>
.btn-github {
  position: sticky;
  top: 10vh;
  left: 90vw;
}
</style>