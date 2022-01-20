<script setup lang="ts">

interface toDoObject {
  title?: string,
  item?: string
}

defineProps<{
  msg?: string,
  toDos: Array<toDoObject>
}>()

const emitObject = <toDoObject>{}

</script>

<template lang="pug">
.wrapper
  h1 {{ msg }}
  br
  input(type="text" placeholder="Title" v-model='emitObject.title')
  input(type="text" placeholder="Item" v-model='emitObject.item')

  button(@click='$emit("add", emitObject )') Add Todo 🔥
  .todo-list
    .list(v-for="todo in toDos")
      span {{ todo.title }}
      p {{ todo.item }}

</template>

<style scoped>
a {
	color: #42b983;
}

label {
	margin: 0 0.5em;
	font-weight: bold;
}

code {
	background-color: #eee;
	padding: 2px 4px;
	border-radius: 4px;
	color: #304455;
}
</style>
