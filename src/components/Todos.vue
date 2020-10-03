<template>
  <div>
    <div :key="todo.id" v-for="todo in todos">
      <TodoItem :todo="todo" v-on:onchange="markComplete" />
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";
export default {
  props: ["todos"],
  components: { TodoItem },
  methods: {
    markComplete({ id }) {
      console.log(id);
    },
  },
};
</script>
