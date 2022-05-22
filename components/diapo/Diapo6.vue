<template>
  <diapo-item>
    <template #title> Stage de 1<sup>ère</sup> année </template>
    <v-col cols="6">
      <card-technologies :logos="['html5.png', 'css.png', 'vue.png']" />
      <card-resume class="my-4">
        <template #title> Difficultés rencontrées</template>
        Planification de mon travail, rester dans les délais impartis.
      </card-resume>
    </v-col>
    <v-col cols="6">
      <card-resume>
        <template #title> Technologies utilisées </template>
        <ul>
          <li>HTML5</li>
          <li>CSS3</li>
          <li>VueJS</li>
        </ul>
        Création d'un site web vitrine avec VueJS pour le compte d'un auto-entrepreneur.
        <br /> Utilisation de Figma pour réaliser les maquettes.
      </card-resume>
      <v-row justify="center" class="my-4"><img v-img:group-6 src="/screenshot_armorprod.png"
          alt="Capture d'écran du site" height="400" /></v-row>
    </v-col>
  </diapo-item>
</template>
