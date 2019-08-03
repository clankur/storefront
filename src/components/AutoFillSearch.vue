<template>
  <v-autocomplete label="Components" :items="getProductNames(productsData)"></v-autocomplete>
</template>

<script lang="js">
export default {
  name: "AutoFillSearch",
  props: ["productsData"],
  methods : {
   getProductNames(productsData){
     const searchData = []
     for (let i = 0; i < productsData.length; i++) {
       searchData.push(productsData[i]['name'])
     }
     return searchData;
   }
  }
};
</script>