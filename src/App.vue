<template>
  <div id="app">
    <img width="25%" src="./assets/logo.png">
    <vue-speedometer :value="toggle ? 333 : 555"/>
    <HelloWorld msg="Hello Vue in CodeSandbox!"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import VueSpeedometer from "vue-speedometer";

export default {
  name: "App",
  created() {
    setInterval(() => (this.toggle = !this.toggle), 1111);
  },
  data() {
    return {
      toggle: false
    };
  },
  components: {
    HelloWorld,
    VueSpeedometer
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
