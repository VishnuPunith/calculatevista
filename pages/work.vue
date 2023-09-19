<template>
<body>
  <div>
    <div class="log">
            <h1 class="head">Work Calculator</h1>

      <div>
        <label for="force" class="value">Force (N):</label>
    <el-input placeholder="Enter Force" v-model="force" @input="calculateWork" class="cm"></el-input>

      </div>
      <div>
        <label for="distance" class="value">Distance (m):</label>
            <el-input placeholder="Enter Distance" v-model="distance" @input="calculateWork" class="cm"></el-input>
      </div>
    </div>
     <div class="result">
      <p class="kilo">Result:{{ result }} </p>
    </div>
  </div>
</body>
</template>

<script>
export default {
  data() {
    return {
      force: null,
      distance: null,
      result: null,
    };
  },
  methods: {
    calculateWork() {
      if (this.force !== null && this.distance !== null) {
        this.result = (this.force * this.distance).toFixed(2);
      } else {
        this.result = null;
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
.result{
    display: flex;
    justify-content: center;
}
</style>