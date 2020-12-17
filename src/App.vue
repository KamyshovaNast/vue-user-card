<template>
  <div id="app">
    <UserCard v-bind:sourse="sourse" v-bind:nickname="nickname" v-bind:name="name" v-bind:adress="adress" v-bind:email="email" v-bind:number="number"/>
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
        return {sourse: '../assets/70.jpg',
        nickname: 'romashka',
        name: 'Иванов Иван Иванович',
        adress: 'Москва, Юбилейная 50',
        email: 'coldrabbit48@example.com',
        number: '+7-495-266-57-34'}
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
