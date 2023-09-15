<template>
    <body>
    <div>
      <h1 class="head">Centimeter to Meters Converter</h1>
      <div class="log">
        <label for="cmInput" class="value">Enter the Centimeter value</label>
        <el-input placeholder="Enter Centimeter" v-model="centimeter" class="cm"></el-input>
        <div>
        <p class="kilo">meters: {{ meters }} m</p>
      </div>
    </div>
     
    </div>
</body>
  </template>
  

  <script>
  export default {
    data() {
      return {
        centimeter: '',
      };
    },
    computed: {
      meters() {
        return (this.centimeter / 100).toFixed(2);
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
  padding: 20px 509px;
}
.cm{
  padding: 12px;
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
}
</style>