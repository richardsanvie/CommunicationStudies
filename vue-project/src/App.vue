  <script setup>
  import { ref } from 'vue';

const number1 = ref(0);
const number2 = ref(0);
const operator = ref('+');
const result = ref(0);

function calculate() {
  if (operator.value === '+') {
    return(result.value = number1.value + number2.value);
  } 
  else if (operator.value === '-') {
    return(result.value = number1.value - number2.value);
  }
}

console.log(calculate())

</script>

<template>
 <div class="container d-flex justify-content-center align-items-center">
  <h1>Calculadora</h1>
  <input type="number" v-model="number1">
  <select  v-model="operator">
    <option value="+">+</option>
    <option value="-">-</option>
  </select>
  <input type="number" v-model="number2">

  <span>Resultado: {{ calculate() }}</span>
 </div>
</template>

<style scoped>
  .container{
    height: 100vh;
  }
</style>


