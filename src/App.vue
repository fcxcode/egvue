<template>
  <b-container fluid id="app">

    <b-row class="header">
      <b-col>
        <img alt="Extreme Games logo" src="./assets/extreme-games-logo.png">          
      </b-col>
    </b-row>

    <b-row class="nav">
      <b-col>
      </b-col>
    </b-row>

    <b-row>
      <b-col class="aside" sm="2">
        <h3>Playerlist</h3>
        <PlayerActivity/>
      </b-col>
      <b-col class="section">
        <h3>Chat</h3>
        <ChatLog/>
      </b-col>
    </b-row>



    <section></section>
    <footer></footer>
    <activities-charts/>
  </b-container>
</template>

<script>
import PlayerActivity from "./components/PlayerActivity.vue";
import ActivitiesCharts from "./components/ActivitiesCharts.vue";
import ChatLog from "./components/ChatLog.vue";
import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue'
Vue.use(BootstrapVue);
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: "app",
  components: {
    PlayerActivity,
    ActivitiesCharts,
    ChatLog
  }
};
</script>

<style>
body{
  background: black;
}

.header{
  height: 100px;
  text-align: center;
  background: #222222;
}

.header img{
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}

.aside{
  padding: 20px 15px;
  background: #121212;
}

.section{
  padding: 20px 15px;
}

h3{
  color: white;
}
</style>
