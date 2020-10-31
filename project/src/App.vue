<template>
  <div id="app" class="main-container" :style="{ backgroundImage: 'url('+require('./assets/'+background)+')' }">
    <UserLoginPage/>
  </div>
  
</template>

<script>
import UserLoginPage from './components/UserLoginPage.vue'

export default {
  name: 'App',
  components: {
    UserLoginPage
  },
  data(){
    return{
      background: 'background.png'
    }
    
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  list-style-type: none;
}
#app {
  font-family: -apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,Noto Sans,sans-serif,Apple Color Emoji,Segoe UI Emoji,Segoe UI Symbol,Noto Color Emoji;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.main-container{
  width: 100vw;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-size: cover;
}
</style>
