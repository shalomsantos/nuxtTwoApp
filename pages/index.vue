<template>
  <v-container>
    <v-container>
      <v-row>
        <v-col cols="12" col="12" md="auto" v-for="(item, i) in items" :key="i">
          <v-card>
            <img src="../assets/carrinho-compras.png" alt="" width="120"/>
            <v-card-title>
              {{ item.text }}
            </v-card-title>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    
    <v-btn color="primary"><v-icon left>mdi-thumb-down</v-icon>button</v-btn>
    <v-btn color="accent"><v-icon left>mdi-thumb-up</v-icon>button</v-btn>
    <v-btn color="secondary"><v-icon left>mdi-cloud-upload </v-icon>button</v-btn>
    <v-btn color="info"><v-icon left>mdi-wrench</v-icon>button</v-btn>
    <v-btn color="warning"><v-icon left>mdi-arrow-left</v-icon>button</v-btn>
    <v-btn color="error"><v-icon left>mdi-checkbox-marked-circle</v-icon>button</v-btn>
    <v-btn color="success"><v-icon left>mdi-cancel</v-icon>button</v-btn>
    <v-btn color="success"><v-icon left>mdi-minus-circle</v-icon>Cancel</v-btn>
    <v-btn color="success"><v-icon>mdi-magnify</v-icon></v-btn>
    <v-btn color="success"><v-icon>mdi-heart</v-icon></v-btn>
    <v-btn color="success"><v-icon>mdi-dots-vertical</v-icon></v-btn>
    <v-btn color="success"><v-icon>mdi-magnify</v-icon></v-btn>
    {{ ip }}
  </v-container>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const ip = await $axios.$get('https://fakestoreapi.com/products/1')
    return { ip }
  },
  data: () => ({
    items: [
      {
        path: '../assets/bebida.png',
        text: 'restaurantes'
      },
      {
        path: '../assets/bebida.png',
        text: 'mercados'
      },
      {
        path: '../assets/bebida.png',
        text: 'farmacias'
      },
      {
        path: '../assets/bebida.png',
        text: 'pets'
      },
      {
        path: '../assets/bebida.png',
        text: 'bebidas'
      },
      {
        path: '../assets/bebida.png',
        text: 'shopping'
      },
      {
        path: '../assets/bebida.png',
        text: 'gourmet'
      },
    ],
  }),
}

</script>