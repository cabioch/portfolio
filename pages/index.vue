<template>
  <div id="main">
    <presentation :page="page" v-scroll="onScrolled" id="presentation" />
    <div id="content">
      <!-- Les différents stages & AP seront ici -->
      <button-source :url="page.url_source" :isVisible="isButtonVisible" />
      <v-carousel hide-delimiters="true" height="100%">
        <diapo-1 />
        <diapo-2 />
        <diapo-3 />
        <diapo-4 />
        <diapo-6 />
        <diapo-5 />
      </v-carousel>
    </div>
  </div>
</template>

<script>
export default {
  // Récupère le contenu de la page
  async asyncData({ $content }) {
    return {
      page: await $content('presentation').fetch(),
    }
  },

  methods: {
    onScrolled(e) {
      const scrollTop = e.target.documentElement.scrollTop
      this.isButtonVisible = scrollTop >= this.scrollMin
    },
  },

  data: () => ({
    scrollMin: Number,
    isButtonVisible: false,
  }),
  mounted: function () {
    // TODO La méthode ne fonctionne pas si la hauteur du viewport change
    // On définit une distance de scroll minimum pour afficher le bouton GitHub
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
  height: 100vh;
  width: 99vw;
}
</style>