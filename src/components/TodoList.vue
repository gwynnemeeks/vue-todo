<template>
  <div>
    <h1>ToDo List</h1>
    <div v-for="item in todos" :key="item.id">
      <todo-item :todo="item" @status-change="handleStatusChange" />
    </div>
  </div>
</template>

<script>
import { todoItems } from "../data";
import TodoItem from "./TodoItem.vue";

export default {
  components: { TodoItem },
  methods: {
    handleStatusChange(item) {
      item.complete = !item.complete;
      console.log(item);
    }
  },
  data() {
    return {
      todos: [...todoItems]
    };
  }
};
</script>

<style></style>
