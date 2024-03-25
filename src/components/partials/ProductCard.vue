<script>
export default {
  props: {
    product: Object,
  },
  methods: {
    getImagePath(img) {
      return new URL(`../../assets/img/${img}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <main>
    <a href="#" class="card">
      <img :src="getImagePath(product.frontImage)" :alt="product.frontImage" />
      <img :src="getImagePath(product.backImage)" alt="product.backImage" class="sec-image" />
      <span class="heart">&hearts;</span>
      <div class="badges">
        <span class="badge disc">-50%</span>
        <span class="badge sost">Sostenibilità</span>
      </div>
      <div class="info">
        <span class="brand">{{ product.brand }}</span>
        <h4 class="prod-title">{{ product.name }}</h4>
        <span class="prod-disc-price">14.99 €</span>
        <span class="prod-price">{{ product.price }} €</span>
      </div>
    </a>
  </main>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;
.card {
  margin-bottom: 20px;
  position: relative;
  &:hover {
    opacity: 0.6;
  }
  &:hover .sec-image {
    display: block;
  }
  img {
    max-width: 320px;
  }
  .prod-title {
    text-transform: uppercase;
  }
  .heart {
    position: absolute;
    background-color: white;
    top: 10px;
    right: 0;
    width: 35px;
    height: 35px;
    font-size: 1.5rem;
    text-align: center;
    &:hover {
      color: red;
    }
  }
  .badges {
    position: absolute;
    bottom: 80px;
    left: 0;
  }
  .badge {
    padding: 5px 10px;
    color: white;
    font-weight: 700;
  }
  .disc {
    background-color: red;
  }
  .sost {
    background-color: #008000;
  }
  .brand {
    font-size: 0.8rem;
  }
  .prod-disc-price {
    color: #ff0000;
    font-weight: 800;
  }
  .prod-price {
    text-decoration: line-through;
  }
  .sec-image {
    display: none;
    position: absolute;
    top: 0;
    left: 0;
  }
}
</style>
