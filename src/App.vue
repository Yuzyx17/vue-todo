<script setup lang="ts">
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue'
import TodoItem from './components/TodoItem.vue';

const todos = ref([
  {
    title: 'a',
    desc: 'a',
    check: false
  },{
    title: 'b',
    desc: 'b',
    check: false
  },{
    title: 'c',
    desc: 'c',
    check: false
  },{
    title: 'd',
    desc: 'd',
    check: true
  },{
    title: 'e',
    desc: 'e',
    check: false
  }
]) 
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />
  <TodoItem v-for="todo in todos" :title=todo.title :desc=todo.desc :check=todo.check />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
