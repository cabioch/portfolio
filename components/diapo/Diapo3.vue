<template>
  <diapo-item>
    <template #title>AP du 3<sup>eme</sup> semestre</template>
    <v-col cols="6">
      <card-resume>
        <p>
          Création d'une application semblable a Doctolib sous Symfony : prise
          de rendez vous, recherche selon la position et la spécialité du
          médecin, ...
          <br />
          Utilisation de MongoDB pour la base de données.
        </p>
      </card-resume>
      <card-resume>
        <template #title> Outils utilisés </template>
        <p>
          <!-- TODO A réécrire ? -->
          <b>Notion : </b> Gestion de projet, notes, etc...
        </p>
        <v-card outlined class="mb-6">
          <img v-img:group-3 src="/screenshot_notion.png" alt="Capture d'écran Notion" width="100%" />
        </v-card>
      </card-resume>
    </v-col>
    <v-col cols="6">
      <card-technologies :height="100" :logos="[
        'symfony.png',
        'mongodb.png',
        'php.png',
        'html5.png',
        'css.png',
        'js.png',
      ]" />
    </v-col>
  </diapo-item>
</template>
