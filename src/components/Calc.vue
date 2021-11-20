<template>
  <div>
    <div class="display">
      <input type="number" v-model.number="operand1" />
      <input type="number" v-model.number="operand2" />
      = {{ result }}
    </div>

    <div>
      <button v-on:click="sum">+</button>
      <button v-on:click="sub">-</button>
      <button v-on:click="div">/</button>
      <button v-on:click="multi">*</button>
      <button v-on:click="degree">degree</button>
      <button v-on:click="intDiv">Integer Division</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Calc',
  data() {
    return {
      operand1: 0,
      operand2: 0,
      result: 0,
    }
  },
  methods: {
    sum() {
      this.result = this.operand1 + this.operand2
    },
    div() {
      this.result = this.operand1 / this.operand2
    },
    sub() {
      this.result = this.operand1 - this.operand2
    },
    multi() {
      this.result = this.operand1 * this.operand2
    },
    degree() {
      this.result = this.operand1 ** this.operand2
    },
    intDiv() {
      if (this.operand1 / this.operand2 >= 0) {
        this.result = Math.floor(this.operand1 / this.operand2)
      } else {
        this.result = Math.ceil(this.operand1 / this.operand2)
      }
    },
  },
}
</script>
