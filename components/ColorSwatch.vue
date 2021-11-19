<template>
  <div class="swatch-container margin-section">
    <div class="product-colors">
      <button class="color-selector">
        <span class="color-item" :class="$paramCase(colorData.id)"></span>
      </button>
    </div>
    <span class="selected-color">{{ colorData.id }}</span>
  </div>
</template>

<script>
export default {
  props: ['colorData']
}
</script>

<style scoped>
.selected-color {
  font-size: 16px;
  line-height: 22.4px;
  letter-spacing: 0.15px;
  font-family: DWFutura,sans-serif;
  font-weight: normal;
}

.color-item {
  border: 0px;
  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  align-items: center;
  margin-right: 0px;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  box-shadow: none;
  min-width: 18px;
}

.rose-gold {
  background: rgb(229, 174, 135);
}

.silver{
  background: rgb(193, 193, 193);
}

.color-selector {
  position: relative;
  background-color: transparent;
  border: none;
  padding: 0px;
  cursor: pointer;
  margin-right: 2rem;
}

.color-selector:after {
  box-sizing: border-box;
  position: absolute;
  content: " ";
  left: -0.2rem;
  top: -0.2rem;
  width: calc(100% + 0.4rem);
  height: calc(100% + 0.4rem);
  border-radius: 50%;
  border: 0.1rem solid rgb(0, 8, 28);
}
</style>
