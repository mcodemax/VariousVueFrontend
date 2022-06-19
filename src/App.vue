<template>
  <h1>Welcome to the VariousVue Listing App!</h1>
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
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
}
</style>
