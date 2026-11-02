<script setup>
const { product } = defineProps({
  product: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <!-- 2. Tambahkan v-if untuk memastikan props.product memiliki data sebelum dirender -->
  <div class="product-card">
    <img :src="product.image" :alt="product.title" class="product-image" />
    <h2 class="product-title">{{ product.title }}</h2>
    <p class="product-description">{{ product.description }}</p>
    <!-- Gunakan optional chaining untuk properti berantai seperti .price.toFixed -->
    <span class="product-price">Rp{{ product.price }}</span>
  </div>
</template>

<style scoped>
/* Style Anda yang sudah ada */
.product-card {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease-in-out;
  cursor: pointer;
}

.product-card:hover {
  transform: scale(1.05);
}

.product-image {
  width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 4px;
  margin-bottom: 10px;
}

.product-title {
  font-size: 18px;
  font-weight: bold;
  margin-bottom: 10px;
}

.product-description {
  color: #555;
  margin-bottom: 10px;
}

.product-price {
  color: #00b894;
  font-weight: bold;
}

/* Tambahan style untuk placeholder */
.product-card-placeholder {
  background-color: #f5f5f5;
  padding: 20px;
  border-radius: 8px;
  text-align: center;
  color: #888;
}
</style>
