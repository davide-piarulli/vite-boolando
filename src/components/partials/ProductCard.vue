<script>
export default {
  props: {
    // ad ogni ciclo ricevo un object
    product: Object,
  },
  methods: {
    getImagePath(img) {
      return new URL(`../../assets/img/${img}`, import.meta.url).href;
    },
  },
  computed: {
    // discountPrice(){
    //   let discountExists = false;
    //   let discount;
    //   let priceDiscount;
    //   this.product.badges.forEach(b => {
    //    if(b.type == 'discount') {
    //     discountExists = true
    //     discount = b.value
    //    }
    //   })
    //   if (discountExists) {
    //     const discountInt =
    //   }
    //   console.log(b.type);
    //   return 'xxx'
    // }
  },
};
</script>

<template>
  <main>
    <div href="#" class="card">
      <img :src="getImagePath(product.frontImage)" :alt="product.frontImage" class="fir-image"/>
      <img :src="getImagePath(product.backImage)" :alt="product.backImage" class="sec-image" />
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
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;
.card {
  margin-bottom: 10px;
  position: relative;
  img {
    max-width: 320px;
  }
  &:hover .sec-image {
    display: block;
  }
  .sec-image {
    display: none;
    position: absolute;
    top: 0;
    left: 0;
  }
  .prod-title {
    text-transform: uppercase;
  }
  .heart {
    position: absolute;
    background-color: $bg-color-main;
    top: 10px;
    right: 0;
    width: 35px;
    height: 35px;
    font-size: 1.5rem;
    text-align: center;
    &:hover {
      color: $icon-heart-hover;
    }
  }
  .badges {
    position: absolute;
    bottom: 80px;
    left: 0;
    .badge {
      padding: 5px 10px;
      color: $text-primary;
      font-weight: 700;
    }
    .disc {
      background-color: $bg-color-discount;
    }
    .sost {
      background-color: $bg-color-tag;
    }
  }
  .brand {
    font-size: 0.8rem;
  }
  .prod-disc-price {
    color: $text-disc-price;
    font-weight: 800;
  }
  .prod-price {
    text-decoration: line-through;
  }
}
</style>
