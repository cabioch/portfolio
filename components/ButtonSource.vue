<template >
  <v-tooltip bottom>
    <template v-slot:activator="{ on }">
      <v-fade-transition hide-on-leave>
        <v-btn
          fab
          fixed
          :href="url"
          target="_blank"
          class="btn-github"
          v-on="on"
          v-show="isVisible"
          transition="scale-transition"
          dark
        >
          <v-icon>mdi-github</v-icon>
        </v-btn>
      </v-fade-transition>
    </template>
    <span>Voir mon code source sur GitHub</span>
  </v-tooltip>
</template>

<script>
export default {
  props: {
    url: String,
    isVisible: Boolean,
  },
}
</script>

<style scoped>
.btn-github {
  top: 5vh;
  left: 95vw;
}
</style>