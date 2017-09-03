<template>
  <div>
    <input type="text" v-model="text">
    <button @click="addFn(text)">Add</button>
  </div>
</template>

<script>
  export default {
    props: {
      addFn: Function,
    },
    data() {
      return {
        text: '',
      }
    }
  }
</script>

<style lang="scss">
</style>
