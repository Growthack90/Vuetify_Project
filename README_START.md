# Start Vuetify

Vuetify è uno dei framework UI più solidi per Vue.js. Si basa su **Material Design**, il che significa che potrai creare interfacce bellissime e professionali senza dover scrivere montagne di CSS personalizzato.

Ecco la tabella di marcia per configurare il tuo ambiente e creare il tuo primo progetto.

---

## 1. Prerequisiti

Assicurati di avere installato **Node.js** (versione LTS consigliata). Puoi verificare aprendo il terminale e digitando:
`node -v`

## 2. Creazione del progetto Vue

Useremo **Vite**, che è lo standard moderno per creare progetti Vue velocemente. Apri il terminale nella cartella dove vuoi salvare il progetto e scrivi:

```bash
npm create vuetify@latest

```

### Durante l'installazione:

Il terminale ti farà alcune domande. Ecco cosa ti consiglio per esercitarti:

1. **Project name:** Scegli un nome (es. `mio-progetto-vuetify`).
2. **Use Essentials or Full:** Scegli **Essentials** (include le basi come router e pinia).
3. **Use TypeScript:** Scegli **No** se vuoi restare sul semplice, **Yes** se vuoi imparare lo standard attuale dell'industria.
4. **Install dependencies with:** Scegli **npm**.

---

## 3. Struttura del Progetto

Una volta terminato, entra nella cartella e avvia il server di sviluppo:

```bash
cd mio-progetto-vuetify
npm run dev

```

Ora apri l'indirizzo che appare (solitamente `http://localhost:3000`). Vedrai la pagina di benvenuto di Vuetify.

---

## 4. I Concetti Chiave per Esercitarti

Per padroneggiare Vuetify, devi capire come ragiona. Ecco i tre pilastri su cui dovresti concentrarti all'inizio:

### A. Il Sistema a Griglia (Grid System)

Vuetify usa un sistema a 12 colonne basato su Flexbox. È fondamentale per rendere il sito responsive.

* `<v-container>`: Centra il contenuto.
* `<v-row>`: Crea una riga.
* `<v-col>`: Definisce quanto spazio occupa un elemento (es. `cols="12" md="6"`).

### B. I Componenti "Pane e Burro"

Inizia a sostituire i tag HTML classici con quelli di Vuetify nel file `App.vue`:

* **Bottoni:** `<v-btn color="primary">Cliccami</v-btn>`
* **Card:** `<v-card title="Titolo" text="Contenuto..."></v-card>`
* **Icone:** `<v-icon icon="mdi-home" />` (Vuetify usa Material Design Icons di default).

### C. Le Props di Stile

Invece di scrivere `style="margin-top: 20px"`, Vuetify usa delle abbreviazioni (Utility Classes):

* `class="mt-5"` (Margin Top 5)
* `class="pa-3"` (Padding All 3)

---

## 5. Un piccolo esercizio pratico

Prova a modificare il file `src/components/HelloWorld.vue` (o crea un nuovo componente) inserendo questo codice per testare la griglia:

```html
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

```

---
