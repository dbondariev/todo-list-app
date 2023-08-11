<template>
  <div>
    <input v-model="newTask" placeholder="Введите задачу" />
    <button @click="addTask">Добавить</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTask: '',
    };
  },
  methods: {
    addTask() {
      if (this.newTask.trim() === '') return;

      this.$store.commit('addTask', { text: this.newTask, completed: false });
      this.newTask = '';
    },
  },
};
</script>
