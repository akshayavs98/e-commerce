<template>
  <div class="product-card">
    <div class="product-image-card">
      <img :src="image" :alt="title" class="product-image" />
      <div class="actions">
        <IconButton :icon="favoriteIcon"></IconButton>
        <IconButton :icon="visibleIcon"></IconButton>
      </div>
      <div class="product-add">Add to cart</div>
    </div>
    <div class="product-title">{{ title }}</div>
    <div class="product-info">
      <div class="product-rate">€{{ price }}</div>
    </div>
  </div>
</template>
<script>
import { defineComponent } from 'vue'
import favoriteIcon from '@/assets/icons/favorite.svg'
import visibleIcon from '@/assets/icons/visible.svg'
import IconButton from './IconButton.vue'

export default defineComponent({
  props: {
    title: String,
    price: Number,
    rating: Object,
    image: String,
    category: String,
    description: String
  },
  components: {
    IconButton
  },
  setup() {
    return {
      favoriteIcon,
      visibleIcon
    }
  }
})
</script>
<style scoped>
.product-image-card {
  position: relative;
  background-color: #fff;
  border: 1px solid #ddd;
  padding: 15px;
  text-align: center;
  width: 15em;
  height: 15em;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.product-image {
  max-width: 60%;
}
.actions {
  position: absolute;
  top: 10px;
  right: 10px;
  display: flex;
  flex-direction: column;
  gap: 0.5em;
}
.product-rate {
  color: red;
}
.product-add {
  display: none;
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: var(--vt-c-black);
  color: var(--vt-c-white);
  padding: 10px;
}
.product-image-card:hover .product-add {
  display: block;
}
.product-title {
  font-weight: 500;
}
</style>
