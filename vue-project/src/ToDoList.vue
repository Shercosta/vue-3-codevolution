<template>
  <div>
    <h2>To Do List Page</h2>
    <pre>Plate: {{ plate }}</pre>
    <ul>
      <li v-for="todo in todos" :key="todo">{{ todo }}</li>
    </ul>

    <div>
      <form @submit.prevent="submitTodo">
        <label for="insert">New Todo:</label>
        <input type="text" name="" id="insert" v-model.lazy="plate" />
        <button type="submit">Add New</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "ToDoList",
  data() {
    return {
      todos: ["Jack", "Ryan", "Gosling"],
      plate: "",
    };
  },
  methods: {
    submitTodo() {
      this.todos.unshift(this.plate);
    },
  },
};
</script>

<style>
</style>