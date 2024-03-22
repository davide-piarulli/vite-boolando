<script>
import ProductCard from "./partials/ProductCard.vue";
import database from "../assets/data/db.json";
export default {
  components: {
    ProductCard
  },
  data() {
    return {
      database,
    };
  },
  mounted() {
    console.log(database);
  },
  methods
};
</script>
<template>
  <section class="container ">
    <div class="row d-flex">

      <ProductCard 
        v-for="product in database.products" :key="product.id"
        frontImg="`src/assets/img/${product.frontImage}`"
        backImg="`src/assets/img/${}`"
      />

    </div>
  </section>
</template>

<style lang="scss" scoped>

</style>
