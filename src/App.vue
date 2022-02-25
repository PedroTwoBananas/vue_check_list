<template>
  <div>
    <TaskForm @create="createTask"/>
    <TaskList :removeTask="removeTask" :tasks="tasks"/>
  </div>
</template>

<script lang="ts">
import TaskForm from "@/components/TaskForm.vue";
import TaskList from "@/components/TaskList.vue"

export default {

  components: {
    TaskForm, TaskList
  },

  data() {
    return {
      tasks: []
    }
  },

  methods: {
    createTask(task) {
      this.tasks.push(task)
    },
    removeTask(task) {
      this.tasks = this.tasks.filter(key => key.id !== task.id)
    }
  }
}
</script>

<style scoped>
div {
  margin: auto 30px;
}
</style>
