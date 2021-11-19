<template>
  <div v-b-hover="handleHover" class="card" :class="isHovered ? 'shadow' : ''">
    <div class="image-container">
      <img
        class="image"
        v-if="productData.images && productData.images[0]"
        :src="productData.images[0].src"
      />
    </div>
    <div class="header-container">
      <h3 class="header margin-section">{{ productData.name }}</h3>
      <ColorSwatch
        v-if="productData.color.id !== 'N/A'"
        :color-data="productData.color"
      />
      <Price
        :price-data="productData.price"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: ['productData'],
  data () {
    return {
      isHovered: false
    }
  },
  methods: {
    handleHover (hovered) {
      this.isHovered = hovered
    }
  }
}
</script>

<style scoped>
.card {
  width: 25%;
  height: 33.5rem;
  border: none;
  overflow: hidden;
  padding-left: 10px;
  padding-right: 10px;
  cursor: pointer;
}

.image {
  border-radius: 0.0rem;
  max-height: 100%;
  max-width: 100%;
  object-fit: contain;
}

.image-container {
  display: flex;
  flex-wrap: wrap;
  height: 400px;
  background-color: #C4CBCB2F;
}

.header {
  font-size: 13px;
  letter-spacing: 2.4px;
  text-transform: uppercase;
  font-family: DWFutura,sans-serif;
  font-weight: normal;
  margin-top: 1.2rem;
}

.header-container {
  height: 100px;
}

</style>
