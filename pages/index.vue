<template>
  <div id="main">
    <presentation :page="page" v-scroll="onScrolled" id="presentation" />
    <div id="content">
      <!-- Les différents stages & AP seront ici -->
      <button-source :url="page.url_source" :isVisible="isButtonVisible" />
      <v-carousel hide-delimiters="true">
        <v-carousel-item>
          <v-card elevation="0" class="px-6 pb-6">
            <v-card-title primary-title class="justify-center text-h3">
              AP du 1<sup>er</sup> semestre
            </v-card-title>
            <v-row>
              <v-col cols="6">
                <technologies
                  :height="100"
                  :test="['html5.png', 'css.png', 'mysql.png']"
                />
              </v-col>
              <v-col cols="6">
                <v-card class="px-4">
                  <v-card-title primary-title class="justify-center">
                    Résumé du projet
                  </v-card-title>
                  <p>
                    Création d'un site présentant un métier lié à
                    l'informatique. Découverte des langages du Web et des bases
                    de données.
                  </p>
                </v-card>
              </v-col>
            </v-row>
          </v-card>
        </v-carousel-item>
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
  height: 100vh;
  width: 99vw;
}
</style>