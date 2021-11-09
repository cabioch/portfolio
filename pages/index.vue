<template>
  <div id="main">
    <Presentation :page="page" />
    <div class="test"></div>
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

<style scoped>
.test {
  height: 100%;
  width: 100%;
}
#main {
  height: 100%;
  width: 100%;
}
</style>