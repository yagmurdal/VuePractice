<script setup>
import { reactive, ref } from 'vue';
const todoInput = ref('')
const todos = reactive([])

const add = () => {
    if (todoInput.value.length) {
        let todo = {
            text: todoInput.value,
            done: false
        }
        todos.push(todo)
        todoInput.value = ''
    }
}

const done = (index) => {
    if (!todos[index]?.done) {
        todos[index].done = true
        let element = todos[index]
        todos.splice(index, 1);
        todos.splice(0, 0, element);
    }
}

const remove = (index) => {
    if (!todos[index].done) {
        todos.splice(index, 1);
    }
}
</script>

<template>
    <input type="text" @keyup.enter="add" v-model="todoInput" />
    <ul>
        <li v-for="(todo, i) in todos" :key="i" :class="todo.done ? 'done' : ''">
            {{ todo.text }}
            <button class="done-btn" v-if="!todo.done" @click="done(i)">Done</button>
            <button class="remove-btn" v-if="!todo.done" @click="remove(i)">Remove</button>
        </li>
    </ul>
</template>

<style scoped>
.done {
    text-decoration: line-through;
    color: green;
}

.done-btn {
    margin-right: 6px;
}

</style>