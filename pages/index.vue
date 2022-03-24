<template>
  <div id="main">
    <presentation :page="page" v-scroll="onScrolled" id="presentation" />
    <div id="content">
      <!-- Les différents stages & AP seront ici -->
      <button-source :url="page.url_source" :isVisible="isButtonVisible" />
      <v-carousel height="100vh" hide-delimiters="true">
        <v-carousel-item>
          <v-card elevation="0" height="100%">
            <v-card-title primary-title class="justify-center">
              AP du 1er A METTRE EN SURTEXTE semesttre
            </v-card-title>
            <v-row>
              <v-col cols="6">
                <v-card>
                  <v-card-title primary-title class="justify-center">
                    test
                  </v-card-title>
                  <v-flex>
                    <img
                      src="/symfony_logo.png"
                      alt="Logo Symfony"
                      height="100px"
                    />
                    <p>Symfony</p>
                  </v-flex>
                </v-card>
              </v-col>
              <v-col cols="6"> col 2 </v-col>
            </v-row>
          </v-card>
        </v-carousel-item>
        <v-caroussel-item> </v-caroussel-item>
      </v-carousel>
    </div>
  </div>
</template>

<script>
import TestArticle from '~/components/TestArticle.vue'
export default {
  components: { TestArticle },
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