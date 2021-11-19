<template>
  <div class="product-price margin-section">
    <span>{{ priceData.amount }}{{ priceData.symbol }}</span>
  </div>
</template>

<script>
export default {
  props: ['priceData']
}
</script>

<style scoped>
.product-price {
  font-size: 16px;
  font-family: DWFutura,sans-serif;
  font-weight: normal;
  letter-spacing: 0.15px;
}
</style>
