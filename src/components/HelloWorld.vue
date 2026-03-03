<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="4" v-for="n in 3" :key="n">
        <v-card
          class="mx-auto"
          elevation="4"
        >
          <v-card-item title="Esercizio Vuetify">
            <template v-slot:subtitle> Card numero {{ n }} </template>
          </v-card-item>
          <v-card-text>
            Sto imparando a usare i componenti di Vuetify!
          </v-card-text>
          <v-card-actions>
            <v-btn variant="tonal" color="secondary">Dettagli</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>

  </v-container>

</template>