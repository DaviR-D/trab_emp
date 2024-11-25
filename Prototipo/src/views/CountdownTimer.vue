<template>
  <div class="countdown-timer">
    <h2>Tempo de uso limite:</h2>
    <div class="input-group">
      <label for="hoursInput">Horas:</label>
      <input
        type="number"
        id="hoursInput"
        v-model.number="inputHours"
        placeholder="Horas"
        min="0"
      />
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
    <button @click="startCountdown" :disabled="isCounting || !isValidTime">Iniciar</button>
    <!--<button @click="resetCountdown" :disabled="!isCounting">Resetar</button>-->

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
    }
  },
  computed: {
    isValidTime() {
      return this.inputHours > 0 || this.inputMinutes > 0
    },
  },
  methods: {
    startCountdown() {
      if (this.isValidTime) {
        // Converte horas e minutos para segundos
        this.remainingTime = this.inputHours * 3600 + this.inputMinutes * 60
        this.isCounting = true
        this.timer = setInterval(() => {
          if (this.remainingTime > 0) {
            this.remainingTime--
          } else {
            this.resetCountdown()
            alert('Tempo esgotado!')
          }
        }, 1000)
      }
    },
    resetCountdown() {
      clearInterval(this.timer)
      this.remainingTime = 0
      this.isCounting = false
      this.inputHours = 0
      this.inputMinutes = 0
    },
    formatTime(seconds) {
      const hrs = Math.floor(seconds / 3600)
      const mins = Math.floor((seconds % 3600) / 60)
      const secs = seconds % 60
      return `${String(hrs).padStart(2, '0')}:${String(mins).padStart(2, '0')}:${String(secs).padStart(2, '0')}`
    },
  },
  beforeUnmount() {
    clearInterval(this.timer)
  },
}
</script>

<style scoped>
.countdown-timer {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.input-group {
  display: flex;
  gap: 10px;
  margin: 10px 0;
}

.display-time {
  font-size: 2em;
  margin-top: 20px;
}

button {
  margin: 5px;
  padding: 8px 16px;
  cursor: pointer;
}

button:disabled {
  cursor: not-allowed;
  opacity: 0.6;
}
</style>
