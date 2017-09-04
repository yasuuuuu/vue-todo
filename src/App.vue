<template>
  <div>
    Todo-list
    <todo-input :addFn="addTodo"></todo-input>
    <todo-list :todos="todos"></todo-list>
  </div>
</template>

<script>
  import TodoInput from './components/Todo/TodoInput.vue';
  import TodoList from './components/Todo/TodoList.vue';
  export default {
    data() {
      return {
        todos: [],
      }
    },
    components: {
      TodoInput,
      TodoList,
    },
    methods: {
      addTodo(text) {
        this.todos.push({ text });
      }
    }
  }
</script>

<style lang="scss">
</style>
