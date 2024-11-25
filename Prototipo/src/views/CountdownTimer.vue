<template>
  <div class="countdown-timer">
    <h2>⏳ Tempo de Uso Limite:</h2>
    <div class="input-group">
      <div class="input-wrapper">
        <label for="hoursInput">Horas:</label>
        <input
          type="number"
          id="hoursInput"
          v-model.number="inputHours"
          placeholder="Horas"
          min="0"
        />
      </div>
      <div class="input-wrapper">
        <label for="minutesInput">Minutos:</label>
        <input
          type="number"
          id="minutesInput"
          v-model.number="inputMinutes"
          placeholder="Minutos"
          min="0"
          max="59"
        />
      </div>
    </div>
    <div class="button-group">
      <button
        class="btn start"
        @click="startCountdown"
        :disabled="isCounting || !isValidTime"
      >
        Iniciar
      </button>
      <!--<button class="btn reset" @click="resetCountdown" :disabled="!isCounting">Resetar</button>-->
    </div>
    <div class="display-time">
      <span>{{ formatTime(remainingTime) }}</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputHours: 0, // Horas inseridas pelo usuário
      inputMinutes: 0, // Minutos inseridos pelo usuário
      remainingTime: 0, // Tempo restante em segundos
      timer: null, // Referência ao setInterval
      isCounting: false, // Estado do cronômetro
    };
  },
  computed: {
    isValidTime() {
      return this.inputHours > 0 || this.inputMinutes > 0;
    },
  },
  methods: {
    startCountdown() {
      if (this.isValidTime) {
        // Converte horas e minutos para segundos
        this.remainingTime = this.inputHours * 3600 + this.inputMinutes * 60;
        this.isCounting = true;
        this.timer = setInterval(() => {
          if (this.remainingTime > 0) {
            this.remainingTime--;
          } else {
            this.resetCountdown();
            alert("Tempo esgotado!");
          }
        }, 1000);
      }
    },
    resetCountdown() {
      clearInterval(this.timer);
      this.remainingTime = 0;
      this.isCounting = false;
      this.inputHours = 0;
      this.inputMinutes = 0;
    },
    formatTime(seconds) {
      const hrs = Math.floor(seconds / 3600);
      const mins = Math.floor((seconds % 3600) / 60);
      const secs = seconds % 60;
      return `${String(hrs).padStart(2, "0")}:${String(mins).padStart(2, "0")}:${String(secs).padStart(2, "0")}`;
    },
  },
  beforeUnmount() {
    clearInterval(this.timer);
  },
};
</script>

<style scoped>
.countdown-timer {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #f9f9f9;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  margin: auto;
  font-family: 'Arial', sans-serif;
}

h2 {
  color: #333;
  margin-bottom: 15px;
}

.input-group {
  display: flex;
  gap: 20px;
  margin: 15px 0;
}

.input-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
}

label {
  margin-bottom: 5px;
  font-size: 0.9em;
  color: #555;
}

input {
  width: 60px;
  padding: 8px;
  text-align: center;
  border: 1px solid #ddd;
  border-radius: 5px;
  font-size: 1em;
  outline: none;
  transition: border-color 0.2s ease;
}

input:focus {
  border-color: #007bff;
}

.display-time {
  font-size: 2.5em;
  color: #007bff;
  margin-top: 20px;
}

.button-group {
  display: flex;
  gap: 10px;
}

button {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  color: white;
  font-size: 1em;
  cursor: pointer;
  transition: background 0.3s ease, transform 0.2s ease;
}

button.start {
  background: #007bff;
}

button.start:disabled {
  background: #a6c8ff;
  cursor: not-allowed;
}

button:hover {
  transform: scale(1.05);
}

button:disabled:hover {
  transform: none;
}

</style>
