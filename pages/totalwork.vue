<template>
<body>
  <div>
    <div class="log">
    <h1>Total Work Calculator</h1>
    <div>
      <label for="forceInput" class="value">Force (N):</label>
           <el-input placeholder="Enter Force Value" v-model="force" @input="calculateTotalWork" class="cm"></el-input>
    </div>
    <div>
      <label for="distanceInput" class="value">Distance (m):</label>
    <el-input placeholder="Enter Distance Value" v-model="distance" @input="calculateTotalWork" class="cm"></el-input>
    </div>
    <div>
      <p class="kilo">Force: {{ force }} N</p>
      <p class="kilo">Distance: {{ distance }} m</p>
      <p class="kilo">Total Work: {{ totalWork }} J</p>
    </div>
  </div>
  </div>
</body>
</template>

<script>
export default {
  data() {
    return {
      force: '',
      distance: '',
      totalWork: null,
    };
  },
  methods: {
    calculateTotalWork() {
      const force = parseFloat(this.force);
      const distance = parseFloat(this.distance);

      if (!isNaN(force) && !isNaN(distance)) {
        this.totalWork = force * distance;
      } else {
        this.totalWork = null;
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