<template>
  <div class="icon-button">
    <img :src="icon" />
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    icon: { type: String, required: true }
  },
  setup() {}
})
</script>
<style scoped>
.icon-button {
  height: 40px;
  width: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: none;
  cursor: pointer;
  background-color: var(--vt-secondary);
  border-radius: 50%;
}
.icon-button:hover {
  background-color: var(--vt-main);
}
</style>
