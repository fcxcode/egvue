<template>
  <div id="app">

    <header class="header">
      <img alt="Extreme Games logo" src="./assets/extreme-games-logo.png">
    </header>

    <nav>

    </nav>

    <section></section>
    <footer></footer>
    <PlayerActivity/>
    <activities-charts/>
  </div>
</template>

<script>
import PlayerActivity from "./components/PlayerActivity.vue";
import ActivitiesCharts from "./components/ActivitiesCharts.vue";

export default {
  name: "app",
  components: {
    PlayerActivity,
    ActivitiesCharts
  }
};
</script>

<style>
header{
  height: 100px;
  background: #000;
}

header img{
  position: relative;
  top: 50%;
  transform: translateY(-50%);
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
