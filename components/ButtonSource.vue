<template>
  <!-- TODO: Ajouter un tooltip -->
  <v-tooltip bottom>
    <template v-slot:activator="{ on }">
      <v-btn fab :href="url" class="btn-github" v-on="on">
        <v-icon>mdi-github</v-icon>
      </v-btn>
    </template>
    <span>Voir mon code source sur GitHub</span>
  </v-tooltip>
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