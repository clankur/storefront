<template>
  <v-app dark>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Car</span>
        <span class="font-weight-light">Shop</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn flat href="#" target="_blank">
        <span class="mr-2">Latest Release</span>
      </v-btn>
    </v-toolbar>

    <v-content>
      <ProductGrid :products="json"></ProductGrid>
    </v-content>
  </v-app>
</template>

<script>
import json from './assets/products.json'
import HelloWorld from './components/HelloWorld'
import ProductGrid from './components/ProductGrid'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ProductGrid,
  },
  data() {
    return {
      json,
    }
  },
}
</script>
