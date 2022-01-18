<template>
  <div id="main">
    <presentation :page="page" />
    <div id="content">
      <!-- Les différents stages & AP seront ici -->
      <button-source :url="page.url_source" />
      <timeline />
    </div>
  </div>
</template>

<script>
import ButtonSource from '~/components/ButtonSource.vue'
import Timeline from '~/components/Timeline.vue'
export default {
  components: { ButtonSource, Timeline },
  async asyncData({ $content }) {
    const page = await $content('presentation').fetch()

    return {
      page,
    }
  },
}
</script>

<style scoped>
#main {
  height: 100vh;
  width: 100vw;
}
#content {
  height: 100%;
  width: 100%;
}
</style>