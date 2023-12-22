<script>
export default {
  name: "ProductItem",
  props: {
    product: Object
  }
};
</script>

<template>
  <div class="product-item">
    <img :src="`/assets/${product.image}`" class="product-image" />
    <p class="product-price">{{ product.price }}</p>
    <i v-if="product.status ==1" class="bi bi-check-circle-fill"></i>
    <i v-else class="bi bi-check-circle"></i>
    <h3>{{ product.name }}</h3>
    <p class="product-description">{{ product.description }}</p>
    <i v-if="product.rating >= 1" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
    <i v-if="product.rating >= 2" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
    <i v-if="product.rating >= 3" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
    <i v-if="product.rating >= 4" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
    <i v-if="product.rating >= 5" class="bi bi-star-fill"></i>
    <i v-else class="bi bi-star"></i>
  </div>
</template>




<style>
.product-item {
  padding: 1rem;
  margin: 1rem;
  width: 300px;
  text-align: center;
}

.product-image {
  max-width: 100%;
  height: auto;
  margin-bottom: 1rem;
}

.product-price {
  color: red;
  font-weight: bold;
  font-size: 1.2rem;
  margin-top: 0.5rem;
}
</style>