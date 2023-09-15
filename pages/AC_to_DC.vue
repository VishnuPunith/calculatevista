<template>
    <body>
    <div>
        <div class="log">
      <h1 class="head">AC to DC Converter Simulation</h1>
      <div>
        <label for="acVoltage" class="value">AC Voltage (Volts):</label>
        <el-input placeholder="Enter AC voltage" v-model="acVoltage" class="cm"></el-input>
      </div>
      <div>
        <button @click="convert">Convert</button>
      </div>
      <div>
        <p class="kilo">DC Voltage (Volts): {{ dcVoltage }}</p>
      </div>
    </div>
    </div>
</body>
  </template>
  
  <script>
  export default {
    data() {
      return {
        acVoltage: '',
        dcVoltage: '',
      };
    },
    methods: {
      convert() {
        const acVoltage = parseFloat(this.acVoltage);
        if (!isNaN(acVoltage)) {
          const dcVoltage = Math.abs(acVoltage); 
          this.dcVoltage = acVoltage*0.636.toFixed(2);
        }
      },
    },
  };
  </script>
  
  <style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
  body{
    background-color: rgba(200, 227, 218, 0.736);
  }
  .log{
    display: flex;
    flex-direction: column;
    width: fit-content;
    align-items: center;
    padding: 20px 386px;
  }
  .cm{
    display: flex;
    padding: 11px 17px;
    size: 1px;
}
  .value{
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
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