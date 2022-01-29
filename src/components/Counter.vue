<!-- js  -->
<script setup>import { ref } from 'vue';

    const number = ref(0)

    const inc = () => {
        number.value ++
    }
</script>

<!-- html -->
<template>
    <button @click="inc">Click</button>
    <span>{{number}}</span>
</template>

<!-- css -->
<style scoped>
    button{
        font-size: 20px;
        margin-right: 20px;
    }
    span{
        font-size: 20px;
    }
</style>

