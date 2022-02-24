<template>
  <ul class="list">
    <TaskItem/>
  </ul>
</template>

<script>
import TaskItem from "@/components/TaskItem";

export default {

  components: {
    TaskItem
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