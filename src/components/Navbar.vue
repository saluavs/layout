<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      absolute
      color="white"
      elevate-on-scroll
      scroll-target="#scrolling-techniques-7"
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Mi App</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn href="#" text>
        <span class="mr-2">Inicio</span>
      </v-btn>
      <v-btn href="#" text>
        <span class="mr-2">Buscar</span>
      </v-btn>
      <v-btn href="#" text>
        <span class="mr-2">Acerca de</span>
      </v-btn>
    </v-app-bar>

    <v-sheet
      id="scrolling-techniques-7"
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 700px;"
        ><v-main class="mt-10">
          <v-container>
            <v-row>
              <v-col
                cols="4"
                v-for="personaje of personajes"
                :key="personaje.id"
              >
                <v-card>
                  <v-img :src="personaje.imagen" height="370px"></v-img>
                  <v-card-title>{{ personaje.nombre }}</v-card-title>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-main>
      </v-container>
    </v-sheet>
  </v-card>
</template>

<script>
export default {
  name: "Navbar",

  data: function() {
    return {
      personajes: [
        {
          id: 1,
          nombre: "Morty",
          imagen: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
        },
        {
          id: 2,
          nombre: "Rick",
          imagen: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
        },
        {
          id: 3,
          nombre: "Summer",
          imagen: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
        },
        {
          id: 4,
          nombre: "Beth",
          imagen: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
        },
        {
          id: 5,
          nombre: "Jerry",
          imagen: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
        },
      ],
    };
  },
};
</script>
