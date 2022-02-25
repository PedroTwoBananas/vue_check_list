<template>
  <div>
    <input
        @keyup.enter="createTask"
        v-model="task.text"
        type="text"
        placeholder="Введите задачу"
    >
    <button @click="createTask">Добавить</button>
  </div>
</template>

<script lang="ts">
export default {

  data() {
    return {
      task: {
        text: '',
      }
    }
  },

  methods: {
    createTask() {
      this.task.id = Date.now();
      this.task.isDone = false;
      this.$emit('create', this.task);
      this.task = {
        text: ''
      }
    }
  }
}

</script>

<style scoped>
div {
  padding: 10px;
  border: 2px solid black;
}
</style>