<template>
  <v-hover>
    <v-card slot-scope="{ hover }" :class="`elevation-${hover ? 24 : 2}`">
      <v-img v-bind:src="product.image" height="12em"></v-img>
      <div>
        <v-card-title>
          <h3 class="headline mb-0">{{product.name}}</h3>
        </v-card-title>
        <v-divider></v-divider>
        <v-list dense>
          <v-list-tile>
            <v-list-tile-content>Price:</v-list-tile-content>
            <v-list-tile-content class="align-end">{{ formatPrice(product.price) }}</v-list-tile-content>
          </v-list-tile>
          <v-list-tile>
            <v-list-tile-content>Miles:</v-list-tile-content>
            <v-list-tile-content class="align-end">{{ product.milage }}</v-list-tile-content>
          </v-list-tile>
        </v-list>
      </div>
    </v-card>
  </v-hover>
</template>

<script lang="js">
  export default  {
    name: 'product-card',
    props: ["product"],
    mounted() {

    },
    data() {
      return {
      }
    },
    methods: {
      formatPrice(value) {
        let val = (value/1).toFixed(2)
        return '$ ' + val.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")
      }
    },
    computed: {

    }
}
</script>