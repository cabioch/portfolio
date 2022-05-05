<template>
  <diapo-item>
    <template #title> Création du Portfolio</template>
    <v-col cols="6">
      <card-resume>
        <p>
          Création de mon portfolio avec NuxtJS (SSR), VueJS et Vuetify. CI Avec
          GitHub. Utilisation de notion pour le suivi du projet. Présenter Nuxt
          ??
          <br />
          AJOUTER LOGOS + Screenshot Notion ?? / Docs de nuxt, ou qqchose ??
        </p>
      </card-resume>
    </v-col>
    <v-col cols="6">
      <card-technologies
        :height="100"
        :logos="[
          'nuxt.png',
          'vue.png',
          'vuetify.png',
          'html5.png',
          'css.png',
          'js.png',
        ]"
      />
    </v-col>
  </diapo-item>
</template>