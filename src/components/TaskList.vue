<template>
  <ul class="list">
    <TaskItem v-for="task in tasks" :key="task.id" :task="task" :removeTask="removeTask"/>
  </ul>
</template>

<script>
import TaskItem from "@/components/TaskItem";

export default {

  components: {
    TaskItem
  },
  props: {
    removeTask: Function,
    tasks: []
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