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
  color: #007bff;
  padding: 10px;
  border-radius: 50%;
  transition: background 0.3s ease, color 0.3s ease;
}



.menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 250px;
  height: 100%;
  background-color: #f0f4f8;
  box-shadow: 2px 0 8px rgba(0, 0, 0, 0.2);
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 15px;
  z-index: 1000;
}

.menu-item {
  display: block;
  font-size: 1.2em;
  padding: 10px 15px;
  color: #333;
  text-decoration: none;
  border-radius: 8px;
  transition: background 0.3s ease, color 0.3s ease;
}

.menu-item:hover {
  background-color: #e9ecef;
  color: #0056b3;
}

@media (max-width: 768px) {
  .hamburger-button {
    top: 15px;
    left: 15px;
    font-size: 20px;
  }

  .menu {
    width: 200px;
    padding: 15px;
  }

  .menu-item {
    font-size: 1em;
    padding: 8px 12px;
  }
}

</style>
