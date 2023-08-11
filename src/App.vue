<template>
  <div id="app">
    <h1>Список задач</h1>
    <AddTask />
    <TaskList />
  </div>
</template>

<script>
import AddTask from './components/AddTask.vue';
import TaskList from './components/TaskList.vue';

export default {
  components: {
    AddTask,
    TaskList,
  },
};
</script>
