<template>
  <v-card>
    <v-card-title primary-title class="justify-center">
      Technologies utilisées
    </v-card-title>
    <v-container>
      <v-row class="py-8">
        <img
          v-for="item in test"
          :key="item"
          :src="'/logos/' + item"
          :height="height + 'px'"
          class="mx-10"
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
    test: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style scoped>
</style>