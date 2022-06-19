<template>
  <APIConnector />
</template>

<script>
import APIConnector from "./components/APIConnector.vue";

export default {
  name: "App",
  components: {
    APIConnector,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  box-sizing: border-box;
  color: #17222c;
  background-color: rgb(193, 193, 158);
  width: 100vw;
  min-height: 100vh;
  padding: 0;
  margin: 0;
}
</style>
