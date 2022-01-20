<script setup lang="ts">
import { reactive } from "vue";
import Test from "./components/TestComponent.vue";


//data
var todos: Array<Object> = reactive([])
var msg = "Hi, we are here to test TS / Vue3 & Composition Api / Vite 🚀"

function addToList(val: Object) {
  todos.push(val)
}
</script>

<template>
	<Test :msg="msg" :toDos="todos" @add="addToList" />
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
