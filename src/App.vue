<template>
  <main>
    <TopBar />
    <div class="view">
      <RouterView />
    </div>
  </main>
</template>

<script setup>
import TopBar from './components/TopBar.vue'
import { RouterView } from 'vue-router'
</script>

<style scoped>
.view {
  margin: 25px;
}
</style>
