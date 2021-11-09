<template>
  <Presentation :page="page" />
</template>

<script>
export default {
  async asyncData({ $content }) {
    const page = await $content('presentation').fetch()

    return {
      page,
    }
  },
}
</script>