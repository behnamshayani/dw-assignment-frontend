<template>
  <ul class="cards-list">
    <LargeProductCard
      v-for="product in allProducts"
      :key="product.sku"
      :product-data="product"
    />
  </ul>
</template>

<script>
export default {
  data () {
    return {
      allProducts: []
    }
  },
  async fetch () {
    this.allProducts = await fetch(
      'https://lw9xczrbgi.execute-api.eu-north-1.amazonaws.com/products'
    ).then(res => res.json())
  }
}
</script>

<style scoped>
.cards-list {
  margin-top: 1.6rem;
  margin-bottom: 0px;
  padding: 0px 0.7rem;
  display: flex;
  flex-flow: row wrap;
  -webkit-box-pack: center;
  justify-content: center;
  list-style: none;
}
</style>
