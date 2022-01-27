<template>
  <!-- Ce composant servira a avoir une timeline dynamique, qui se modifie quand on scroll sur le site -->
  <!-- https://vuetifyjs.com/en/components/timelines/ -->
  <v-timeline>
    <v-timeline-item> Projets de 1<sup>ère</sup> année </v-timeline-item>
    <v-timeline-item large></v-timeline-item>
  </v-timeline>
</template>

<style scoped>
* {
  color: black;
}
/* TODO Transition entre large ou pas (sera utilisé pour savoir lequel est sélectionné), et cliquable pour accéder aux "chapitres" */
</style>