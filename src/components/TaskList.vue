<template>
  <ul class="list">
    <TaskItem @check="checkTask" @remove="deleteTask" v-for="task in tasks" :key="task.id" :task="task"/>
  </ul>
</template>

<script>
import TaskItem from "@/components/TaskItem";

export default {
  props: {
    tasks: []
  },

  components: {
    TaskItem
  },
  methods: {
    deleteTask(task) {
      this.$emit('remove', task)
    },
    checkTask(task) {
      this.$emit('remove', task)
    }
  }
}

</script>

<style scoped>

.list {
  margin-top: 20px;
  padding: 10px;
  height: 100vh;
  border: 2px solid black;
}

</style>