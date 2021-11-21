<template>
  <ul class="cards-list">
    <LargeProductCard
      v-for="product in allProductsInfo"
      :key="product.sku"
      :product-data="product"
    />
  </ul>
</template>

<script>
import { allProducts } from '@/assets/data.js'

export default {
  data () {
    return {
      allProductsInfo: allProducts
    }
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
