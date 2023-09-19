<template>
<body>
  <div>
    <div class="log">
    <h1 class="head">Wavelength Calculator</h1>
    <div>
      <label for="frequencyInput" class="value">Frequency (Hz):</label>
           <el-input placeholder="Enter Frequency" v-model="frequency" @input="calculateWavelength" class="cm"></el-input>

    </div>
    <div>
      <label for="waveSpeedInput" class="value">Wave Speed (m/s):</label>
    <el-input placeholder="Enter WaveSpeed" v-model="waveSpeed" @input="calculateWavelength" class="cm"></el-input>

    </div>
    <div>
      <p class="kilo">Frequency: {{ frequency }} Hz</p>
      <p class="kilo">Wave Speed: {{ waveSpeed }} m/s</p>
      <p class="kilo">Wavelength: {{ wavelength }} m</p>
    </div>
    </div>
  </div>
</body>
</template>

<script>
export default {
  data() {
    return {
      frequency: '',
      waveSpeed: '',
      wavelength: null,
    };
  },
  methods: {
    calculateWavelength() {
      const frequency = parseFloat(this.frequency);
      const waveSpeed = parseFloat(this.waveSpeed);

      if (!isNaN(frequency) && !isNaN(waveSpeed) && frequency > 0 && waveSpeed > 0) {
        this.wavelength = waveSpeed / frequency;
      } else {
        this.wavelength = null;
      }
    },
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
body{
  background-color: rgba(200, 227, 218, 0.736);
}
.log{
  display: flex;
  flex-direction: column;
  width: fit-content;
  align-items: center;
  padding: 20px 509px;
}
.cm{
  padding: 12px;
  size: 1px;
}
.value{
  font-family: 'Poppins', sans-serif;
  font-weight: 600;
      padding: 12px;

}
.kilo{
  font-family: 'Poppins', sans-serif;
  font-weight: 600;
}
.head{
  font-family: 'Poppins', sans-serif;
  display: flex;
  justify-content: center;
  padding: 15px;
  white-space: nowrap;
}
</style>