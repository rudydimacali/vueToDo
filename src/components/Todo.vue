<template>
  <div class="todo">
    <h1>VueToDo</h1>
    <input class="addTodo"
      placeholder="Add Todo"
      v-model="newTodo"
      @keyup.enter="addTodo">
    <ul class="todoList">
      <li v-for="todo in todos"
        :key="todo"
        class="todo"> {{ todo }}
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Todo',
  data() {
    return {
      todos: [],
    };
  },
  methods: {
    addTodo: function () {
      const value = this.newTodo;
      this.todos.push(value);
    },
  },
};


</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
