<template>
  <nav class="nav-links">
    <router-link to="/" class="link" active-class="active">Home</router-link>
    <router-link to="/about" class="link" active-class="active">About</router-link>
    <router-link to="/contact" class="link" active-class="active">Contact</router-link>
    <router-link to="/sign-in" class="link" active-class="active">Sign-in</router-link>

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
  transition: color 0.3s ease;
  flex-grow: 1;
  justify-content: center;
  margin: 0 2em;
}
.link {
  text-decoration: none;
  color: var(--vt-c-black);
}

.link:hover {
  color: var(--vt-main);
  cursor: pointer;
  background-color: transparent;
}

/* Style for the active link */
.active {
  color: var(--vt-main);
  text-decoration: underline;
  text-underline-offset: 10px;
}
</style>
