<template>
      <div class="splash-container">
        <div class="splash">
          <h1>Splendid Food</h1>
        </div>
      </div>

      <main class="wrapper">
        <h2>Recommended</h2>
        <div class="recommended">
          <ProductCard
            v-for="(product, index) in inventory"
            :key="product.id"
            class="card"
            :index="index"
            :product="product"
            :addToCart="addToCart"
          >
          </ProductCard>
        </div>
      </main>
</template>

<script>
import ProductCard from '../components/ProductCard'
export default {
  props: ['inventory', 'addToCart', 'total'],
  name: 'Home',
  components: {
    ProductCard
  }
}
</script>
