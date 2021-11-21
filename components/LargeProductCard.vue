<template>
  <li class="card-item">
    <a v-b-hover="handleHover" class="card-link" :class="isHovered ? 'shadow' : ''" href="#">
      <div class="image-container">
        <img
          v-if="productData.images && productData.images[0]"
          class="image"
          loading="lazy"
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
    </a>
  </li>
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
.card-item {
  width: 25%;
  display: flex;
  padding: 0px 0.7rem;
  margin-bottom: 2rem;
  border: none;
}

.card-link {
  display: flex;
  flex-direction: column;
  align-items: normal;
  width: 100%;
  color: rgb(0, 8, 28);
  text-decoration: none;
  padding: 0 0 2.2rem;
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
