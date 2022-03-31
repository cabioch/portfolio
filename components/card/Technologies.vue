<template>
  <v-card>
    <v-card-title primary-title class="justify-center">
      Technologies utilisées
    </v-card-title>
    <v-container>
      <v-row class="px-8" justify="center">
        <img
          v-for="logoName in logos"
          :key="logoName"
          :src="'/logos/' + logoName"
          :height="height + 'px'"
          class="mx-10 my-4"
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