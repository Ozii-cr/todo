<template>
  <div id="app">
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
  </div>
</template>

<script>
import Todos from "./components/Todos";

export default {
  name: "App",
  components: {
    Todos,
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          Title: "Todo One",
          Completed: false,
        },
        {
          id: 2,
          Title: "Todo Two",
          Completed: false,
        },
        {
          id: 3,
          Title: "Todo Three",
          Completed: false,
        },
      ],
    };
  },
  methods: {},
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
</style>
