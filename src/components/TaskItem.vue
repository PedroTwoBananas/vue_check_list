<template>
  <li class="item">
    <input v-if="!task.isDone" @input="checkTask" type="checkbox">
    <span :class="{completed: task.isDone}">{{task.text}}</span>
    <button @click="deleteTask">x</button>
  </li>
</template>

<script>
export default {
  props: {
    task: {},
  },

  methods: {
    checkTask() {
      this.$emit('check', this.task)
    },
    deleteTask() {
      this.$emit('remove', this.task)
    }
  }
}
</script>

<style scoped>

.item {
  margin-top: 10px;
  border: 2px solid black;
  padding: 12px;
  list-style: none;
}

.completed {
  text-decoration: line-through;
}
</style>