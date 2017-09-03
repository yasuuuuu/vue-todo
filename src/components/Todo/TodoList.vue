<template>
  <ul>
    <template v-for="todo in todos">
      <todo-list-item :todo="todo"></todo-list-item>
    </template>
  </ul>
</template>

<script>
  import TodoListItem from './TodoListItem.vue';
  export default {
    props: {
      todos: Array,
    },
    components: {
      TodoListItem,
    }
  }
</script>

<style lang="scss">
</style>
