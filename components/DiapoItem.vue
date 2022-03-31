<template>
  <v-carousel-item>
    <v-card elevation="0" class="px-6">
      <v-card-title primary-title class="justify-center text-h3">
        <slot name="title">AP du X<sup>ème</sup> semestre </slot>
      </v-card-title>
      <v-row>
        <slot></slot>
      </v-row>
    </v-card>
  </v-carousel-item>
</template>

<script>
export default {}
</script>

<style>
</style>