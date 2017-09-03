<template>
  <div>
    <Header></Header>
    <TodoInput :addFn="addTodo"></TodoInput>
    <TodoList :todos="todos"></TodoList>
  </div>
</template>

<script>
  import Header from './components/Shared/Header.vue';
  import TodoInput from './components/Todo/TodoInput.vue';
  import TodoList from './components/Todo/TodoList.vue';
  export default {
    data() {
      return {
        todos: [],
      }
    },
    components: {
      Header,
      TodoInput,
      TodoList,
    },
    methods: {
      addTodo(text) {
        this.todos.push({
          text: text,
        });
      }
    }
  }
</script>

<style lang="scss">

</style>
