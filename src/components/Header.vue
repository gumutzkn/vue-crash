<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      :text="!showAddTask ? 'Add Task' : 'Close'"
      :color="!showAddTask ? 'green' : 'red'"
      @btn-click="$emit('btn-click')"
    />
  </header>
</template>

<script>
import Button from "./Button";

export default {
  name: "Header",
  props: {
    title: String,
    showAddTask: Boolean,
  },
  components: {
    Button,
  },
  emits: ["btn-click"],
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
