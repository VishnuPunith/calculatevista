<template>
<body>
  <div>
    <div class="log">
    <h1 class="head">Inch to Feet Converter</h1>
    <div>
      <label for="inchInput" class="value">Inches:</label>
      <el-input placeholder="Enter Inches" v-model="inchValue" class="cm"></el-input>
    </div>
    <div>
      <p class="kilo">Feet: {{ feetValue }}</p>
    </div>
  </div>
  </div>
</body>
</template>

<script>
export default {
  data() {
    return {
      inchValue: '',
    };
  },
  computed: {
    feetValue() {
      return (this.inchValue * 0.0833333).toFixed(2);
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
}
</style>