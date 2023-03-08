<script setup>
import { ref } from "vue";
const count = ref(0);

console.log(count.value);

const increaseCount = () => {
  count.value = count.value + 1;
};

const decreaseCount = () => {
  count.value = count.value - 1;
};
</script>

<template>
  <main>
    <div>
      <h3>Current count:</h3>
      <h1>{{ count }}</h1>
      <button @click="decreaseCount">-</button>
      <button @click="increaseCount">+</button>
    </div>
  </main>
</template>

<style scoped>
main {
  background-color: aliceblue;
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

main div {
  text-align: center;
}

h1 {
  font-size: 4rem;
}

h3 {
  font-size: 3rem;
}

button {
  font-size: 1.5rem;
  padding: 0.5rem;
  width: 20%;
  margin-right: 1rem;
  margin-left: 1rem;
  cursor: pointer;
}
</style>
