<template>
  <div class="search-bar">
    <img src="@/assets/icons/search.svg" alt="Search Icon" />
    <input type="text" placeholder="Search for products..." />
    <!-- Search Icon -->
  </div>
</template>
<script>
import { defineComponent } from 'vue'

export default defineComponent({
  setup() {}
})
</script>
<style scoped>
/* Search bar */
.search-bar {
  display: flex;
  align-items: center;
  border: 1px solid #ddd;
  border-radius: 28px;
  padding: 0 24px;
}

.search-bar input {
  border: none;
  padding: 8px;
  outline: none;
  font-size: 16px;
}

.search-bar button {
  background-color: #ff5a5f;
  border: none;
  padding: 8px;
  color: white;
  cursor: pointer;
  border-radius: 0 4px 4px 0;
}
</style>
