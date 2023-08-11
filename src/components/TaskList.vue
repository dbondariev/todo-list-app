<template>
  <div>
    <ul>
      <li v-for="(task, index) in tasks" :key="index">
        <input type="checkbox" v-model="task.completed" />
        {{ task.text }}
        <button @click="removeTask(index)">Удалить</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  computed: {
    tasks() {
      return this.$store.state.tasks;
    },
  },
  methods: {
    removeTask(index) {
      this.$store.commit('removeTask', index);
    },
  },
};
</script>
