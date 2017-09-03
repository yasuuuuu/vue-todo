<template>
  <li v-if="isShow">
    <input type="checkbox" v-model="todoChecked">
    <span :class="{ gray: todoChecked }">{{ todo.text }}</span>
    <button @click="deleteTodo">Delete</button>
  </li>
</template>

<script>
  export default {
    props: {
      todo: Object,
    },
    data() {
      return {
        todoChecked: false,
        isShow: true,
      }
    },
    methods: {
      deleteTodo() {
        this.isShow = false;
      }
    }
  }
</script>

<style lang="scss" scoped>
  .gray {
    color: gray;
  }
</style>
