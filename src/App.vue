<template>
  <div id="app">
    <UserCard v-bind:userCard="userCard"/>
    <button v-on:click="getUserData()">Обновить</button>
  </div>
</template>

<script>
import UserCard from './components/UserCard.vue'

export default {
  name: 'App',
  components: {
    UserCard
  },
  data() {
        return {
            userCard: {}
        }
  },
  methods: {
    getUserData() {
        this.axios
        .get("http://37.77.104.246/users/getrandom.php")
        .then((response) => {this.userCard = response.data})
    }
  },
  mounted() {
    this.getUserData();
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
