<template>
  <div id="app">
    <header-component/>
    <br>
    <img alt="Vue logo" src="./assets/nieva.jpg" />
    <HelloWorld msg="D11" />
    <teamComponetVue/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import HeaderComponent from "./components/headerComponent.vue";
import teamComponetVue from './components/teamComponet.vue';

export default {
  name: "App",
  components: {
    HelloWorld,
    HeaderComponent,
    teamComponetVue

  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

img {
  width: 25%;
  height: 25%;
}
</style>
