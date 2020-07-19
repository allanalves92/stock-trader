<template>
  <v-layout row wrap>
    <stock
      v-for="stock in stockPortfolio"
      :key="stock.id"
      :stock="stock"
    ></stock>
  </v-layout>
</template>

<script>
  import { mapGetters } from 'vuex';
  import Stock from './Stock';
  export default {
    components: {
      Stock,
    },
    computed: {
      ...mapGetters(['stockPortfolio']),
    },
  };
</script>

<style></style>
