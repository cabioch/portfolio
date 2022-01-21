<template>
  <div id="main">
    <presentation :page="page" v-scroll="onScrolled" id="presentation" />
    <div id="content">
      <!-- Les différents stages & AP seront ici -->
      <button-source :url="page.url_source" :isVisible="isButtonVisible" />
      <timeline />
    </div>
  </div>
</template>

<script>
export default {
  // Récupère le contenu de la page
  async asyncData({ $content }) {
    const page = await $content('presentation').fetch()
    return {
      page,
    }
  },

  methods: {
    onScrolled(e) {
      const scrollTop = e.target.documentElement.scrollTop
      if (scrollTop >= this.scrollMin) {
        this.isButtonVisible = true
        return
      }
      this.isButtonVisible = false
    },
  },

  data: () => ({
    scrollMin: Number,
    isButtonVisible: false,
  }),
  mounted: function () {
    // TODO La méthode ne fonctionne pas si la hauteur du viewport change
    this.scrollMin = window.innerHeight / 10
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