<template>
  <div>
    <h3>Todos</h3>
    <Todos :todos="todos" />
    <Test v-on:buttonpressed="buttonpressed" />
    <Test1 v-on:buttonpressed="buttonpressed" />
  </div>
</template>

<script>
import Todos from "./components/Todos";
// import Test1 from "./components/Test1";
// import Test from "./components/Test";
import externalComponents from "./utils/externalComponent";
const Test = () => externalComponents("http://localhost:5500/Test.umd.min.js");
const Test1 = () =>
  externalComponents("http://localhost:5500/Test1.umd.min.js");
export default {
  name: "App",
  components: { Todos, Test, Test1 },
  methods: {
    buttonpressed(msg) {
      console.log(msg);
    },
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "tittle One",
          completed: true,
        },
        {
          id: 2,
          title: "tittle Two",
          completed: false,
        },
        {
          id: 3,
          title: "tittle Three",
          completed: false,
        },
        {
          id: 4,
          title: "tittle four",
          completed: false,
        },
      ],
    };
  },
};
</script>

<style></style>
