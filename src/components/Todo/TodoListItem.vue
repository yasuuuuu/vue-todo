<template>
  <li v-if="isShow">
    <input type="checkbox" v-model="isChecked">
    <span :class="{ checked: isChecked }">{{ todo.text }}</span>
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
        isChecked: false,
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
  .checked {
    color: lightgray;
  }
</style>
