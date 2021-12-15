<template>
  <div id="main">
    <Presentation :page="page" />
    <div id="content">
      <!-- Les différents stages & AP seront ici -->
    </div>
  </div>
</template>

<script>
import ButtonSource from '~/components/ButtonSource.vue'
export default {
  components: { ButtonSource },
  async asyncData({ $content }) {
    const page = await $content('presentation').fetch()

    return {
      page,
    }
  },
}
</script>

<style scoped>
#content {
  height: 100%;
  width: 100%;
}
#main {
  height: 100%;
  width: 100%;
}
</style>