<template>
  <div>
    <input type="checkbox" :checked="todo.completed" @change="onchange" />
    <label>{{todo.title}}</label>
  </div>
</template>

<script>
export default {
  props: ["todo"],
  methods: {
    onchange() {
      this.todo.completed = !this.todo.completed;
      this.$emit("onchange", this.todo);
    }
  }
};
</script>
