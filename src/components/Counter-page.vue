<template>
  <div class="page">
    <h1 class="title">Counter Page</h1>
    <p class="text-size">Counter: {{ number }}</p>
    <div class="buttons">
      <button class="button" @click="increments">Increment</button>
      <button class="button" @click="decrements">Decrement</button>
      <button class="button" @click="reset">Reset</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const number = ref(0);

  function increments() {
        return number.value++;
    }
    function decrements() {
        return number.value--;
    }
    function reset() {
        return number.value = 0;
    }

</script>

<style scoped>
.page {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  font-family: Arial, sans-serif;
  color: #333;
  background-color: #d0caca;
}
.title {
  font-size: 2rem;
  margin-bottom: 1rem;
}
.button {
  padding: 0.5rem 1rem;
  font-size: 1rem;
  background-color: #333;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
.button {
  margin-right: 0.5rem;
}
.text-size {
  font-size: 1.5rem;
}
</style>
