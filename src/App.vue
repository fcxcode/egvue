<template>
  <div id="app">

    <header class="header">
      <img alt="Extreme Games logo" src="./assets/extreme-games-logo.png">
    </header>
    <nav>
    </nav>
    <aside>
      <h3>Playerlist</h3>
      <PlayerActivity/>
    </aside>
    <section></section>
    <footer></footer>
    <activities-charts/>
  </div>
</template>

<script>
import PlayerActivity from "./components/PlayerActivity.vue";
import ActivitiesCharts from "./components/ActivitiesCharts.vue";
import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue'
Vue.use(BootstrapVue);
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: "app",
  components: {
    PlayerActivity,
    ActivitiesCharts
  }
};
</script>

<style>
body{
  background: black;
}

p {
  text-align: left;
}

p span{
    float: right;
}

header{
  height: 100px;
  background: #000; 
}

header img{
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}



aside{
  width: 10%;
  float: left;
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
