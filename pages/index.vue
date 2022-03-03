<template>
  <div id="main">
    <presentation :page="page" v-scroll="onScrolled" id="presentation" />
    <div id="content">
      <!-- Les différents stages & AP seront ici -->
      <button-source :url="page.url_source" :isVisible="isButtonVisible" />
      <v-container fluid>
        <v-row>
          <v-col cols="2">
            <timeline />
          </v-col>
          <v-spacer />
          <v-col cols="8">
            <v-card>
              <test-article :document="aps3" class="p-2" />
              <test-article :document="stage1" class="p-2" />
            </v-card>
          </v-col>
          <v-spacer />
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  // Récupère le contenu de la page
  async asyncData({ $content }) {
    return {
      page: await $content('presentation').fetch(),
      aps3: await $content('projets/APS3').fetch(),
      stage1: await $content('projets/Stage1').fetch(),
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
  height: 100%;
  width: 100%;
}
</style>