<template>
  <UserLoginPage/>
</template>

<script>
import UserLoginPage from './components/UserLoginPage.vue'

export default {
  name: 'App',
  components: {
    UserLoginPage
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
