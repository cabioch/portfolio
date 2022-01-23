<template>
  <nuxt-content :document="document" />
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