<template>
  <div class="container">
    <div class="cards-container">
      <LargeProductCard
        v-for="product in allProductsInfo"
        :key="product.sku"
        :product-data="product"
      />
    </div>
  </div>
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

.container {
  margin-top: 2rem;
  max-width: 1440px;
}
.cards-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
</style>
