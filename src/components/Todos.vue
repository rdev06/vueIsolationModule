<template>
  <div>
    <div :key="todo.id" v-for="todo in todos">
      <TodoItem :todo="todo" @onChange="$emit('onchange', todo.id)" />
    </div>
  </div>
</template>

<script>
  import TodoItem from './TodoItem';
  export default {
    props: ['todos'],
    components: { TodoItem }
  };
</script>
