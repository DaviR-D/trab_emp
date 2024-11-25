<script setup>
import { RouterView } from 'vue-router'
import HamburgerMenu from './components/HamburgerMenu.vue'
</script>

<template>
  <div class="menu-button">
    <HamburgerMenu />
  </div>
  <div class="app-container">
    <RouterView />
  </div>
</template>

<style scoped>
.menu-button {
  display: flex;
  flex-direction: column;
  gap: 4px;
  border: none;
  background: transparent;
  cursor: pointer;
  padding: 0;
  position: absolute;
  top: 10px;
  left: 10px;
}

.app-container {
  margin: 0 auto; /* Centraliza horizontalmente */
  padding: 20px;
}
</style>
