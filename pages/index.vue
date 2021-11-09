<template>
  <div>
    <Presentation :page="page" />
  </div>
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