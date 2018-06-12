<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Demo1></Demo1>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Demo1 from "./pages/demo1.vue";
export default {
  name: "app",
  components: {
    HelloWorld,
    Demo1
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
