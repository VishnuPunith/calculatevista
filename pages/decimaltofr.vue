<template>
<body>
  <div>
    <div class="log">
    <h1 class="head">Decimal to Fraction Converter</h1>
    <div>
      <label for="decimalInput" class="value">Enter a Decimal:</label>
     <el-input placeholder="Enter Decimal Value" v-model="decimalInput" @input="convertToFraction" class="cm"></el-input>
    </div>
    <div>
      <p class="kilo">Decimal: {{ decimalInput }}</p>
      <p class="kilo">Fraction: {{ fraction }}</p>
    </div>
  </div>
  </div>
</body>
</template>

<script>
export default {
  data() {
    return {
      decimalInput:'',
      fraction: '',
    };
  },
  methods: {
    convertToFraction() {
      const decimal = this.decimalInput;
      const fraction = this.toFraction(decimal);
      this.fraction = fraction;
    },
    toFraction(decimal) {
      const tolerance = 1.0e-9;
      let h1 = 1;
      let h2 = 0;
      let k1 = 0;
      let k2 = 1;
      let b = decimal;
      do {
        const a = Math.floor(b);
        let aux = h1;
        h1 = a * h1 + h2;
        h2 = aux;
        aux = k1;
        k1 = a * k1 + k2;
        k2 = aux;
        b = 1 / (b - a);
      } while (Math.abs(decimal - h1 / k1) > decimal * tolerance);

      return `${h1}/${k1}`;
    },
  },
};
</script>
