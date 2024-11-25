<template>
  <div class="tool-grid">
    <h1>Ferramentas para Controle do Tempo Digital</h1>
    <div class="grid-container">
      <a href="https://www.apple.com/screen-time/" target="_blank" class="grid-item">
        <span>Screen Time</span>
      </a>
      <a href="https://www.forestapp.cc/" target="_blank" class="grid-item">
        <span>Forest</span>
      </a>
      <a href="https://www.focusatwill.com/" target="_blank" class="grid-item">
        <span>Focus@Will</span>
      </a>
      <a href="https://www.rescuetime.com/" target="_blank" class="grid-item">
        <span>RescueTime</span>
      </a>
      <a
        href="https://chrome.google.com/webstore/detail/stayfocusd/laankejkbhbdhmipfmgcngdelahlfoji"
        target="_blank"
        class="grid-item"
      >
        <span>StayFocusd</span>
      </a>
      <a href="https://www.proginosko.com/leechblock/" target="_blank" class="grid-item">
        <span>LeechBlock</span>
      </a>
      <a href="https://habitica.com/" target="_blank" class="grid-item">
        <span>Habitica</span>
      </a>
      <a href="https://toggl.com/track/" target="_blank" class="grid-item">
        <span>Toggl Track</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ToolGrid',
}
</script>

<style scoped>
.tool-grid {
  max-width: 800px;
  margin: auto;
  padding: 20px;
  font-family: Arial, sans-serif;
  color: #fff;
  text-align: center;
}

h1 {
  font-size: 2em;
  margin-bottom: 20px;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 20px;
}

.grid-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #333;
  padding: 20px;
  border-radius: 10px;
  text-decoration: none;
  color: #fff;
  transition: transform 0.2s ease;
}

.grid-item:hover {
  transform: scale(1.05);
  background-color: #444;
}

.grid-item i {
  font-size: 2.5em;
  margin-bottom: 10px;
}

.grid-item span {
  font-size: 1.1em;
}
</style>
