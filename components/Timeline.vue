<template>
  <!-- Ce composant servira a avoir une timeline dynamique, qui se modifie quand on scroll sur le site -->
  <!-- https://vuetifyjs.com/en/components/timelines/ -->
  <v-timeline class="testclass">
    <v-timeline-item> Projets de 1<sup>ère</sup> année </v-timeline-item>
    <v-timeline-item></v-timeline-item>
  </v-timeline>
</template>

<style scoped>
.testclass {
  height: 100vh;
}
</style>