<!-- js  -->
<script setup>
import { ref } from 'vue';
const color = ref('')




</script>

<!-- html -->
<template>
    <div :style="{ backgroundColor: color }">
        <input type="text" v-model="color" />
    </div>
</template>

<!-- css -->
<style scoped>
</style>

