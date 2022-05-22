<template>
  <diapo-item>
    <template #title>AP du 2<sup>eme</sup> semestre</template>
    <v-col cols="6">
      <card-technologies :height="100" :logos="[
        'html5.png',
        'css.png',
        'mysql.png',
        'php.png',
        'bootstrap.png',
      ]" />
      <v-card outlined class="ma-5">
        <img v-img:group-2 src="/screenshot_ap2.png" alt="Screenshot du projet numéro 2" width="100%" />
      </v-card>
    </v-col>
    <v-col cols="6">
      <card-resume>
        <p>
          Réalisation d'un site de suivi de stage, avec une partie importante
          sur la sécurité & le RGPD. Projet de groupe fait a 5. Projet réalisé
          en méthode Agile avec deux livraisons.
          <br />
          <b>Outils utilisés : </b> Trello pour la gestion de projet; Cahier des
          charges avec maquettes, test cases & user stories
        </p>
        <v-row justify="center">
          <img v-img:group-2 src="/testcase.png" alt="Image d'un exemple de Test Case" height="200px" />
          <img v-img:group-2 src="/screenshot_trello.png" alt="Livraison sur Trello" height="200px" />
          <img v-img:group-2 src="/screenshot_scenarii.png" alt="User Case" height="200px" />
        </v-row>
      </card-resume>
    </v-col>
  </diapo-item>
</template>
