<template>
  <v-container>
    <div class="d-flex ma-4">
      <h1>{{ page.nom }}</h1>
    </div>
    <div class="">
      <nuxt-content :document="page" />
    </div>
  </v-container>
</template>

<script>
export default {
  props: {
    page: {
      required: true,
    },
  },
}
</script>