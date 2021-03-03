<template>
  <div>
    <h2>{{ todo.name }}</h2>
    <button>Mark Completed</button>
  </div>
</template>

<script>
export default {
  props: ["todo"]
};
</script>

<style scoped>
div {
  border: 3px solid tomato;
  margin: 15px;
  padding: 10px;
}
</style>
