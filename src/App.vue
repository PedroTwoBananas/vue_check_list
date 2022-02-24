<template>
  <div>
    <TaskForm />
    <TaskList/>
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

  }
}
</script>

<style scoped>
div {
  margin: auto 30px;
}
</style>
