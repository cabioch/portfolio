<template>
  <v-tooltip bottom>
    <template v-slot:activator="{ on }">
      <v-btn fab fixed :href="url" target="_blank" class="btn-github" v-on="on">
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
/* TODO Afficher progressivement le bouton */
.btn-github {
  top: 90vh;
  left: 95vw;
}
</style>