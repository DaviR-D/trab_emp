<template>
  <div class="tool-grid">
    <h1>Ferramentas para Controle do Tempo Digital</h1>
    <div class="grid-container">
      <a href="https://www.apple.com/screen-time/" target="_blank" class="grid-item">
        <span>⏰ Screen Time</span>
      </a>
      <a href="https://www.forestapp.cc/" target="_blank" class="grid-item">
        <span>🌳 Forest</span>
      </a>
      <a href="https://www.focusatwill.com/" target="_blank" class="grid-item">
        <span>🎧 Focus@Will</span>
      </a>
      <a href="https://www.rescuetime.com/" target="_blank" class="grid-item">
        <span>📅 RescueTime</span>
      </a>
      <a
        href="https://chrome.google.com/webstore/detail/stayfocusd/laankejkbhbdhmipfmgcngdelahlfoji"
        target="_blank"
        class="grid-item"
      >
        <span>🚫 StayFocusd</span>
      </a>
      <a href="https://www.proginosko.com/leechblock/" target="_blank" class="grid-item">
        <span>⏳ LeechBlock</span>
      </a>
      <a href="https://habitica.com/" target="_blank" class="grid-item">
        <span>🏋️ Habitica</span>
      </a>
      <a href="https://toggl.com/track/" target="_blank" class="grid-item">
        <span>📊 Toggl Track</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "ToolGrid",
};
</script>

<style scoped>
.tool-grid {
  max-width: 900px;
  margin: auto;
  padding: 20px;
  border-radius: 15px;
  background: #f0f4f8;
  color: #333;
  font-family: "Arial", sans-serif;
  line-height: 1.8;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

h1 {
  font-size: 2.2em;
  text-align: center;
  color: #007bff;
  margin-bottom: 30px;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 20px;
}

.grid-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: #e9ecef;
  text-decoration: none;
  color: #333;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, background 0.3s ease;
}

.grid-item:hover {
  transform: scale(1.05);
  background: #dbe2e8;
}

.grid-item span {
  font-size: 1.2em;
  font-weight: 600;
  text-align: center;
  color: #0056b3;
}

@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  }

  .grid-item {
    padding: 15px;
  }

  .grid-item span {
    font-size: 1em;
  }
}


</style>


