<template>
  <diapo-item>
    <template #title> Création du Portfolio</template>
    <v-col cols="6">
      <card-resume>
        <p>
          Création de mon portfolio avec VueJS et Vuetify. Intégration continue avec
          GitHub Actions.
        </p>
      </card-resume>
    </v-col>
    <v-col cols="6">
      <card-technologies :height="100" :logos="[
        'vue.png',
        'vuetify.png',
        'html5.png',
        'css.png',
        'js.png',
      ]" />
    </v-col>
  </diapo-item>
</template>