<template>
  <diapo-item>
    <template #title> AP du 4<sup>ème</sup> semestre </template>
    <v-col cols="6">
      <card-resume>
        <p>
          Création d'une application mobile de gestion d'enchères avec Xamarin, récupération des données a partir d'une
          API codée sous Symfony.
          Utilisation de Notion pour la gestion du projet (<a
            href="https://cabioch.notion.site/62e561f0cbce4452b5b877debdbb98e9?v=a4718bb6688d40e8b7a04a817bf47cc8">Tableau
            kanban</a>) et de Insomnia pour tester les points d'API.
          Réalisation de tests unitaires avec xUnit.

        </p>
      </card-resume>
      <card-resume>
        <template #title>Difficultés rencontrées</template>
        <p>
        <ul>
          <li>Transformer des données d'une API en données utilisables par une application</li>
          <li>Combiner des données d'une API distante et d'une base de données locale</li>
          <li>Utiliser un langage de templating très différent de ceux que je connaissais (XAML)</li>
        </ul>
        </p>
      </card-resume>
      <v-row justify="center" class="mt-4">
        <img v-img:group-4 src="/screenshot_ap4.png" alt="Capture d'écran de l'application" height="400" />
      </v-row>
    </v-col>
    <v-col cols="6">
      <card-technologies :height="100" :logos="[
        'csharp.png',
        'xamarin.png',
        'php.png',
        'symfony.png',
      ]" />
    </v-col>
  </diapo-item>
</template>