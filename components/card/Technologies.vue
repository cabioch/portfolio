<template>
  <v-card>
    <v-card-title primary-title class="justify-center">
      Technologies utilisées
    </v-card-title>
    <v-container>
      <v-row class="py-8">
        <img
          v-for="logoName in logos"
          :key="logoName"
          :src="'/logos/' + logoName"
          :height="height + 'px'"
          class="mx-10"
          :alt="logoName"
        />
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  props: {
    height: {
      type: Number,
      default: 100,
    },
    logos: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style scoped>
</style>