<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Counter from "./components/Counter.vue";
import Todo from "./components/Todo.vue";
import ColorFlipper from "./components/ColorFlipper.vue";
</script>

<template>
  <h1>Mini Projects with Vue 3.2</h1>
  <h2>Counter</h2>
  <Counter />
  <hr />
  <h2>To Do</h2>
  <Todo />
  <hr />
  <h2>Color Flipper</h2>
  <ColorFlipper />
  <hr />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
