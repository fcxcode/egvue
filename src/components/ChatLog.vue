<template>
  <div class="chatlog" v-if="chats && chats.length">
    <div class="message-container" v-for="chats of chats" v-bind:key="chats.message">
      <b-col sm="1" class="chat-messenger">{{chats.name}}</b-col><b-col sm="11" class="chat-message">{{chats.message}}</b-col>
    </div>
  </div>

  <div class="chatlog" v-else-if="errors && errors.length">
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
      chats: [],
      errors: []
    }
  },
  created() {
    axios.get('http://egvue.extreme-games.net:8081/egwebapi/v1/pubinfo')
    .then(response => {   
      this.chats = response.data.chats;
    })
    .catch(e => {
      this.errors.push(e)
    })
  }
}
</script>

<style>
  .message-container{
    margin-bottom: 0px;
    color: #ffbe2c;
  }

  .chat-messenger{
    width: 100px;
    overflow: hidden;
    text-align: right;
    float: left;
    height: 24px;
  }

  .chat-message:before {
    content: "→";
  }

  .chat-message{
    display: inline-block;
  }
</style>