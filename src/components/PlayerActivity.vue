<template>

  <div class="player-listing" v-if="users && users.length">
    <div v-for="users of users" v-bind:key="users.name">
      <p>{{users.name}} <span>{{users.shipType}}</span></p>
    </div>
  </div>

  <div class="player-listing" v-else-if="errors && errors.length">
    <div v-for="error of errors" v-bind:key="error.message">
      <p>{{error.message}}</p>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  data() {
    return {
      users: [],
      errors: []
    }
  },
  created() {
    axios.get('http://egvue.extreme-games.net:8081/egwebapi/v1/pubinfo')
    .then(response => {   
      this.users = response.data.users;
    })
    .catch(e => {
      this.errors.push(e)
    })
  }
}
</script>