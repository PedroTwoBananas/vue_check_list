<template>
  <div>
    <input
        v-model="task.text"
        type="text"
        placeholder="Введите задачу"
    >
    <button>Добавить</button>
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

  methods: {}
}

</script>

<style scoped>
div {
  padding: 10px;
  border: 2px solid black;
}
</style>