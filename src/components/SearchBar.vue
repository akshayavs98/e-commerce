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
  background-color: var(--vt-secondary);
}

.search-bar input {
  border: none;
  padding: 8px;
  outline: none;
  font-size: 16px;
  background-color: var(--vt-secondary);
}
</style>
