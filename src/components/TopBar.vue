<template>
  <header class="topbar">
    <div class="logo">
      <a href="/">MyShop</a>
      <!-- Logo/Brand -->
    </div>
    <NavBar></NavBar>
    <SearchBar></SearchBar>
    <div class="icons">
      <IconButton :icon="shoppingCartIcon"></IconButton>
      <IconButton :icon="profileIcon"></IconButton>
    </div>
  </header>
</template>

<script>
import { defineComponent } from 'vue'
import SearchBar from './SearchBar.vue'
import IconButton from './IconButton.vue'
import NavBar from './NavBar.vue'
import profileIcon from '@/assets/icons/profile.svg'
import shoppingCartIcon from '@/assets/icons/shopping-cart.svg'

export default defineComponent({
  components: {
    SearchBar,
    IconButton,
    NavBar
  },
  setup() {
    return {
      profileIcon,
      shoppingCartIcon
    }
  }
})
</script>

<style scoped>
/* Top bar container */
.topbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #ffffff;
  gap: 1em;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

/* Logo */
.logo a {
  font-size: 24px;
  color: #333;
  text-decoration: none;
  font-weight: bold;
}

/* Icons */
.icons {
  display: flex;
  align-items: center;
  gap: 1em;
}

.cart-count {
  position: absolute;
  top: -8px;
  right: -10px;
  background-color: #ff5a5f;
  color: white;
  border-radius: 50%;
  padding: 2px 6px;
  font-size: 12px;
}

/* Responsive Design */
@media (max-width: 768px) {
  .search-bar {
    flex-grow: 1;
  }

  .nav-links {
    display: none; /* Optionally hide for mobile, replace with hamburger menu */
  }
}
</style>
