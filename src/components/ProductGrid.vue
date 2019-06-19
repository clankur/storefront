<template lang="html">
     <v-layout row wrap>
        <v-flex 4 8 v-for="p in products" :key="n" xs12 sm8 md4 lg2 pa-1>
          <ProductCard :product=p></ProductCard>
        </v-flex>
      </v-layout>
</template>

<script lang="js">
  import ProductCard from './ProductCard'
  
  export default  {
    name: 'product-grid',
    props: ["products"],
    components: {
      ProductCard,
    },
    mounted() {

    },
    data() {
      return {

      }
    },
    methods: {

    },
    computed: {

    }
}
</script>

