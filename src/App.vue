<script setup>
import { ref } from "vue";

const text = ref('');
const awesome = ref(true)
const klik = () => {
  awesome.value = !awesome.value
}
// const onInput = (e) =>{
//   text.value = e.target.value
// }
</script>

<template>
  <input v-model=text>
  <h1>{{ text }}</h1> 
  <h2 v-if="awesome">Kondisi True</h2>
  <h2 v-else>Kondisi False</h2>

  <button @click="klik">klik disini</button>
</template>

<style>
button {
  padding: 10px;
  font-size: 16px;
  background-color: #6610f2;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #4e0dcf;
}
</style>
