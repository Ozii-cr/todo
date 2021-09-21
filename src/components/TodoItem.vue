<template>
  <div class="todoItem" v-bind:class="{ iscomplete: todo.Completed }">
    <p>
      <input type="checkbox" v-on:change="markComplete" />
      {{ todo.Title }}
      <button @click="$emit('del-todo', todo.id)" class="del">x</button>
    </p>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  data() {
    return {
      Todo: this.todo,
    };
  },
  methods: {
    markComplete() {
      this.Todo.Completed = !this.Todo.Completed;
    },
  },
};
</script>

<style scoped>
.todoItem {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #ccc dotted;
}

.iscomplete {
  text-decoration: line-through;
}

.del {
  background: #ff0000;
  color: #fff;
  border: none;
  padding: 5px 9px;
  border-radius: 50%;
  cursor: pointer;
  float: right;
}
</style>