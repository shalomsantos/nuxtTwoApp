<template>
  <v-app>
    <v-card elevation="1" class="rounded-0 px-3 py-2">
      <v-toolbar elevation="0">
        <v-app-bar-nav-icon class="ml-2">
          <img src="../assets/ifood.png" alt="" width="50">
        </v-app-bar-nav-icon>
        <v-sheet class="d-flex pl-8 pr-3" style="gap: 0.8rem;">
          <NuxtLink class="body-2" to="/">Início</NuxtLink>
          <NuxtLink class="body-2" to="/restaurantes">Restaurantes</NuxtLink>
          <NuxtLink class="body-2" to="/mercados">Mercados</NuxtLink>
          <NuxtLink class="body-2" to="/bebidas">Bebidas</NuxtLink>
          <NuxtLink class="body-2" to="/farmacias">Farmácias</NuxtLink>
          <NuxtLink class="body-2" to="/pets">Pets</NuxtLink>
          <NuxtLink class="body-2" to="/shopping">Shopping</NuxtLink>
        </v-sheet>
        <v-col cols="12" sm="6" md="3">
          <v-text-field
            outlined
            label="Buscar por item ou loja"
            prepend-inner-icon="mdi-magnify"
            dense
            filled
            hide-details="auto"
          ></v-text-field>
        </v-col>
        <v-btn class="text-none" color="grey" text>
          {{ adress }}
          <v-icon right color="red">mdi-menu-down</v-icon>
        </v-btn>
        <v-btn elevation="0" color="transparent"><v-icon color="red">mdi-exit-to-app</v-icon></v-btn>

        <div class="d-flex justify-center align-center">
          <v-icon color="red">mdi-basket-outline</v-icon>
          <div class="mt-4 ml-4">
            <p class="mb-n6 text-none body-2">R${{ money }}</p><br>
            <p class="text-none body-2">{{ valor }} itens</p>
          </div>
        </div>
      </v-toolbar>
    </v-card>
    <v-main>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>  
</template>

<script setup>
const adress = 'R. júlio silva, 261';
const money = 54.24;
const valor = 2;
</script>

<style scoped>
a{
  color: grey;
  text-decoration: none;
}
.nuxt-link-exact-active {
  color: red !important;
}
</style>