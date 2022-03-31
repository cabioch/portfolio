<template>
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
        l'informatique, puis mise en commun du travail de chacun. Découverte des
        langages du Web et des bases de données.
      </card-resume>
    </v-col>
    <v-col cols="6">
      <card-resume>
        <template #title> Difficultés rencontrées </template>
        <ul>
          <li>Centralisation et utilisation des bases de données</li>
          <li>Collaboration à partir d'un projet individuel</li>
        </ul>
      </card-resume>
    </v-col>
  </diapo-item>
</template>