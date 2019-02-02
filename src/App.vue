<template>
  <div id="app">

    <header class="header">
      <img alt="Extreme Games logo" src="./assets/extreme-games-logo.png">
    </header>

    <nav>

    </nav>

    <section></section>
    <footer></footer>
    <activities-charts title="Extreme Games"/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import ActivitiesCharts from "./components/ActivitiesCharts.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    ActivitiesCharts
  }
};
</script>

<style>
header{
  height: 100px;
  background: #000;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
