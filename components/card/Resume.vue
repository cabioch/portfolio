<template>
  <v-card class="px-4">
    <v-card-title primary-title class="justify-center">
      <slot name="title">Résumé du projet</slot>
    </v-card-title>
    <slot></slot>
  </v-card>
</template>

<script>
export default {}
</script>