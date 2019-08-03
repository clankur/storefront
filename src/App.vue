<template>
  <v-app dark>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Car</span>
        <span class="font-weight-light">Shop</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <Modal :modalData="modalContent"></Modal>
    </v-toolbar>
    <v-content>
      <AutoFillSearch :productsData="productsData"></AutoFillSearch>
      <ProductGrid :products="productsData"></ProductGrid>
    </v-content>
  </v-app>
</template>

<script>
import productsData from "./assets/products.json";
import modalContent from "./assets/modalContent.json";
import AutoFillSearch from "./components/AutoFillSearch";
import ProductGrid from "./components/ProductGrid";
import Modal from "./components/Modal";

export default {
  name: "App",
  components: {
    ProductGrid,
    Modal,
    AutoFillSearch
  },
  data() {
    console.log(Object.keys(productsData));
    return {
      productsData: productsData,
      modalContent: modalContent,
    };
  },
  getProductNames() {}
};
</script>
