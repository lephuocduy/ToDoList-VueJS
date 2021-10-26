<template>
  <div>
    <todo-list :todos="todos"></todo-list>
    <create-todo @create-todo="addTodo"></create-todo>
  </div>
</template>

<script>
import TodoList from "./components/TodoList.vue";
import CreateTodo from "./components/CreateTodo.vue";

export default {
  name: "app",
  components: {
    TodoList,
    CreateTodo
  },
  data() {
    return {
      todos: []
    };
  },
  methods: {
    addTodo(title) {
      this.todos.push({
        title,
        done: false
      });
      console.log(this.todos);
    }
  }
};
</script>
