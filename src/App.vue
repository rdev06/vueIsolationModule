<template>
  <div>
    <h3>Todos</h3>
    <Todos :todos="todos" />
    <Test />
    <Test1 />
  </div>
</template>

<script>
import Todos from "./components/Todos";
import externalComponents from "./utils/externalComponent";
const Test = () => externalComponents("http://localhost:5500/Test.umd.min.js");
const Test1 = () => externalComponents("http://localhost:5500/Test1.umd.min.js");
export default {
  name: "App",
  components: { Todos, Test, Test1 },
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
