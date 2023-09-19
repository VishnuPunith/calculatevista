<template>
  <div>
    <h1>Work Calculator</h1>
    <div class="log">
      <div>
        <label for="force">Force (N):</label>
        <input v-model="force" type="number" id="force" />
      </div>
      <div>
        <label for="distance">Distance (m):</label>
        <input v-model="distance" type="number" id="distance" />
      </div>
    </div>
    <button @click="calculateWork">Calculate Work (Joules)</button>
    <div class="result" v-if="result !== null">
      <p>Result:</p>
      <p>{{ result }} W</p>
    </div>
  </div>
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