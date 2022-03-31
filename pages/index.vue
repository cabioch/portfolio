<template>
  <div id="main">
    <presentation :page="page" v-scroll="onScrolled" id="presentation" />
    <div id="content">
      <!-- Les différents stages & AP seront ici -->
      <button-source :url="page.url_source" :isVisible="isButtonVisible" />
      <v-carousel hide-delimiters="true" height="100%">
        <diapo-item>
          <template #title> AP du 1<sup>er</sup> semestre </template>
          <v-col cols="6">
            <card-technologies
              :height="100"
              :logos="['html5.png', 'css.png', 'mysql.png']"
            />
          </v-col>
          <v-col cols="6">
            <card-resume>
              Création individuelle d'un site présentant un métier lié à
              l'informatique, puis mise en commun du travail de chacun.
              Découverte des langages du Web et des bases de données.
            </card-resume>
          </v-col>
        </diapo-item>
        <diapo-item>
          <template #title>AP du 2<sup>eme</sup> semestre</template>
          <v-col cols="6">
            <card-technologies
              :height="100"
              :logos="[
                'html5.png',
                'css.png',
                'mysql.png',
                'php.png',
                'bootstrap.png',
              ]"
            />
          </v-col>
          <v-col cols="6">
            <card-resume>
              <p>
                Réalisation d'un site de suivi de stage, avec une partie
                importante sur la sécurité & le RGPD. Projet de groupe fait a 5.
                <br />
                <b>Outils utilisés : </b> Trello, Cahier des charges, test cases
                & user stories
              </p>
              <img src="/logos/trello.png" alt="Logo Trello" height="100px" />
              [Mettre screenshot cahier des charges / site]
            </card-resume>
          </v-col>
          <v-col cols="12">
            <img src="/projets/ap2.png" alt="Screenshot du projet numéro 2" />
            [Mettre screenshot site]
          </v-col>
        </diapo-item>
        <diapo-item>
          <template #title>AP du 3<sup>eme</sup> semestre</template>
          <v-col cols="6">
            <card-resume>
              <p>
                Création d'un clone de Doctolib avec le framework Symfony.
                Utilisation de MongoDB pour la base de données.
              </p>
            </card-resume>
          </v-col>
          <v-col cols="6">
            <card-technologies
              :height="100"
              :logos="[
                'symfony.png',
                'mongodb.png',
                'php.png',
                'html5.png',
                'css.png',
                'js.png',
              ]"
            />
          </v-col>
          <v-col cols="6">
            <card-resume>
              <template #title> Outils utilisés </template>
              <p>
                <!-- TODO A réécrire ? -->
                <b>Notion : </b> Gestion de projet, notes, etc...
              </p>
            </card-resume>
          </v-col>
        </diapo-item>
        <diapo-item>
          <template #title> AP du 4<sup>ème</sup> semestre </template>
        </diapo-item>
        <diapo-item>
          <template #title> Stage de 1<sup>ère</sup> année </template>
        </diapo-item>
        <diapo-item>
          <template #title> Création du Portfolio</template>
        </diapo-item>
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