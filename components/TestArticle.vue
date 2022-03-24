<template>
  <v-card>
    <nuxt-content :document="document" />
  </v-card>
</template>

<script>
export default {
  props: {
    document: {
      required: true,
    },
  },
}
</script>

<style scoped>
* {
  background-color: black;
  color: white;
}
</style>