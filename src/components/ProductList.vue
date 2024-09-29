<template>
  <div class="products-list">
    <ProductCard v-for="product in products" :key="product.id" v-bind="product"> </ProductCard>
  </div>
</template>
<script>
import { defineComponent, ref, computed, onMounted } from 'vue'
import ProductCard from './ProductCard.vue'
import axios from 'axios'

export default defineComponent({
  components: {
    ProductCard
  },
  setup() {
    const products = ref()
    const displayedProducts = ref()
    const isLoading = ref(false)
    const hasMoreProducts = computed(() => {
      if (Array.isArray(displayedProducts) && Array.isArray(products)) {
        return displayedProducts.value.length === products.value.length
      }
      return false
    })

    const fetchProducts = () => {
      axios
        .get('https://fakestoreapi.com/products')
        .then((response) => {
          if (response.data.length > 0) {
            products.value = response.data
          }
        })
        .catch((error) => {
          console.log('error fetching data')
        })
    }

    onMounted(() => {
      fetchProducts()
    })

    return {
      hasMoreProducts,
      isLoading,
      products
    }
  }
})
</script>
<style scoped>
.products-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 20px;
}
</style>
