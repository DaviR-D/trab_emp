<template>
  <div>
    <button @click="toggleMenu" class="hamburger-button">☰</button>
    <div v-if="isOpen" class="menu">
      <router-link to="/" class="menu-item" @click.native="toggleMenu">Home</router-link>
      <router-link to="/timer" class="menu-item" @click.native="toggleMenu">Timer</router-link>
      <router-link to="/tools" class="menu-item" @click.native="toggleMenu">Tools</router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    }
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen
    },
  },
}
</script>

<style scoped>
.hamburger-button {
  position: fixed;
  top: 20px;
  left: 20px;
  font-size: 24px;
  cursor: pointer;
  background: none;
  border: none;
  color: white;
}

.menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 200px;
  height: 100%;
  background-color: #333;
  padding: 20px;
}

.menu-item {
  display: block;
  padding: 10px;
  color: white;
  text-decoration: none;
  font-size: 18px;
}

.menu-item:hover {
  background-color: #444;
}
</style>
