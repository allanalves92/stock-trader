<template>
  <v-layout row wrap>
    <stock v-for="stock in stocks" :key="stock.id" :stock="stock"></stock>
  </v-layout>
</template>

<script>
  import Stock from '@/components/stocks/Stock';
  import { mapGetters } from 'vuex';
  export default {
    components: {
      Stock,
    },
    computed: {
      ...mapGetters(['stocks']),
    },
  };
</script>

<style></style>
