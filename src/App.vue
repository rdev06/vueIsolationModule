<template>
  <div>
    <h3>Todos</h3>
    <Todos :todos="todos" />
    <Test />
  </div>
</template>

<script>
import Todos from "./components/Todos";
import externalComponents from "./utils/externalComponent";
const Test = () => externalComponents("http://localhost:8080/Test.umd.min.js");
export default {
  name: "App",
  components: { Todos, Test },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "tittle One",
          completed: true
        },
        {
          id: 2,
          title: "tittle Two",
          completed: false
        },
        {
          id: 3,
          title: "tittle Three",
          completed: false
        },
        {
          id: 4,
          title: "tittle four",
          completed: false
        }
      ]
    };
  }
};
</script>

<style></style>
