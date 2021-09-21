<template class= "todoitem">
  <div>Todo Item</div>
</template>

<script>
export default {
  name: "TodoItem",
};
</script>

<style scoped>
.todoItem {
  background: white;
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