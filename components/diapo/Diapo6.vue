<template>
  <diapo-item>
    <template #title> Stage de 1<sup>ère</sup> année </template>
    <v-col cols="6">
      <card-technologies :logos="['html5.png', 'css.png', 'vue.png']" />
    </v-col>
    <card-resume>
      <template #title> Technologies utilisées </template>
      <ul>
        <li>HTML5</li>
        <li>CSS3</li>
        <li>VueJS</li>
      </ul>
      Création d'un site web vitrine avec VueJS.
    </card-resume>
    <card-resume>
      Parler des difficultés rencontrées -> Communication, délai et organisation
    </card-resume>
  </diapo-item>
</template>