<script setup>
import { ref } from 'vue';

// State variables
const count = ref(0);
const clickCount = ref(0);

// Increment function
const increment = () => {
  count.value += 1;
  clickCount.value += 1;
};

// Decrement function
const decrement = () => {
  count.value -= 1;
  clickCount.value += 1;
};
</script>

<template>
  <div class="home">
    <h2>Welcome to the Home Page</h2>
    <p>Click the buttons below to increase or decrease the counter:</p>
    <div class="counter-box">
      <div class="button-container">
        <button @click="decrement" class="button decrement">-</button>
        <button @click="increment" class="button increment">+</button>
      </div>
      <p class="counter">Count: {{ count }}</p>
      <p class="click-info">Total Clicks: {{ clickCount }}</p>
    </div>
  </div>
</template>

<style>
.home {
  min-height: 85vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #f4f4f4;
  font-family: Arial, sans-serif;
  padding: 20px;
  text-align: center;
}

h2 {
  font-size: 2rem;
  margin-bottom: 10px;
  color: #333;
}

p {
  margin-bottom: 7px;
  color: #555;
}

.counter-box {
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  width: 300px;
  text-align: center;
}

.button-container {
  display: flex;
  justify-content: center;
  gap: 15px;
  margin-bottom: 20px;
}

.button {
  width: 50px;
  height: 50px;
  font-size: 1.5rem;
  font-weight: bold;
  color: white;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 0.3s ease-in-out;
}

.button.increment {
  background-color: #4caf50;
}

.button.increment:hover {
  background-color: #45a049;
}

.button.decrement {
  background-color: #f44336;
}

.button.decrement:hover {
  background-color: #e53935;
}

.counter {
  font-size: 1.8rem;
  font-weight: bold;
  color: #333;
  margin-bottom: 10px;
}

.click-info {
  font-size: 1rem;
  color: #666;
}
</style>
