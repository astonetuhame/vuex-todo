<template>
  <div class="container">
    <AddTodo />
    <FilterTodos />
    <Todos />
  </div>
</template>

<script>
import Todos from "./components/Todos.vue";
import AddTodo from "./components/AddTodo.vue";
import FilterTodos from "./components/FilterTodos.vue";

export default {
  name: "App",
  components: {
    Todos,
    FilterTodos,
    AddTodo,
  },
};
</script>

<style>
body {
  font-family: "Franklin Gothic Medium", "Arial Narroe", Arial, sans-serif;
  line-height: 1.6;
  background: #e8f7f0;
}

.container {
  max-width: 1100px;
  margin: auto;
  overflow: auto;
  padding: 0 2 rem;
}
</style>
