<template>
  <nav class="nav-links">
    <div class="link">Home</div>
    <div class="link">About</div>
    <div class="link">Contact</div>
    <div class="link">Sign Up</div>
    <!-- <ul>
        <li><a href="/shop">Shop</a></li>
        <li><a href="/deals">Deals</a></li>
        <li><a href="/categories">Categories</a></li>
      </ul> -->
  </nav>
</template>
<style scoped>
/* Navigation Links */
.nav-links {
  display: flex;
  list-style: none;
  flex-direction: row;
  gap: 3em;
  color: #000;
  transition: color 0.3s ease;
  flex-grow: 1;
  justify-content: center;
  margin: 0 2em;
}

.link:hover {
  color: red;
  cursor: pointer;
}
</style>
