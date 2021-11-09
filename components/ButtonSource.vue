<template>
  <!-- TODO: Ajouter un tooltip -->
  <v-btn fab :href="url">
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