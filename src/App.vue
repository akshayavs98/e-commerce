<template>
  <main>
    <TopBar />
    <RouterView />
  </main>
</template>

<script setup>
import TopBar from './components/TopBar.vue'
import { RouterView } from 'vue-router'
</script>
