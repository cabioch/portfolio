<template>
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
          Réalisation d'un site de suivi de stage, avec une partie importante
          sur la sécurité & le RGPD. Projet de groupe fait a 5.
          <br />
          <b>Outils utilisés : </b> Trello, Cahier des charges, test cases &
          user stories
          <img
            src="/logos/trello.png"
            alt="Logo Trello"
            height="30px"
            class="d-inline"
          />
        </p>
        <img
          src="/testcase.png"
          alt="Image d'un exemple de Test Case"
          height="200px"
        />
      </card-resume>
    </v-col>
    <v-col cols="12">
      <img
        src="/screenshot_ap2.png"
        alt="Screenshot du projet numéro 2"
        height="50%"
      />
      [Mettre screenshot site]
    </v-col>
  </diapo-item>
</template>