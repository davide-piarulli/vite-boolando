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
  // methods
};
</script>
<template>
  <section class="container ">
    <div class="row d-flex">

      <!-- :frontImg="`/src/assets/img/${product.frontImage}`" -->
      <ProductCard 
        v-for="product in database.products" :key="product.id"
        :product="product"
        :brand="product.brand"
        :name="product.name"
        :price="product.price"
      />

    </div>
  </section>
</template>

<style lang="scss" scoped>

</style>
