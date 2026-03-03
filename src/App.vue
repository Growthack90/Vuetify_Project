<script setup>
  // 1. IMPORTA il componente dal percorso corretto
  import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <v-app>

    <v-app-bar title="Il mio primo progetto Vuetify"></v-app-bar>

    <v-main>
      <v-container>

        <v-btn color="primary">
          Ciao, sono un bottone Vuetify!
        </v-btn>

        <v-card
          width="400"
          title="Benvenuto nell'esercizio"
          subtitle="Questo è il mio primo elemento reale"
          text="Vuetify rende la creazione di interfacce molto veloce grazie ai componenti pronti all'uso."
          variant="elevated"
          class="mx-auto mt-10"
        >
          <v-card-actions>
            <v-btn variant="text" color="secondary">Scopri di più</v-btn>
            <v-spacer></v-spacer> <v-btn variant="tonal" color="primary">Inizia</v-btn>
          </v-card-actions>
        </v-card>

      </v-container>

      <v-container>

        <HelloWorld />

      </v-container>

    </v-main>
    
  </v-app>
  
</template>