<template>
  <div class="login-form_container">
    <UserSignupForm />
  </div>
</template>

<script>
import UserSignupForm from '@/components/UserSignupForm'

export default {
  components: {
    UserSignupForm
  },
  name: 'UserLoginPage',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.login-form_container{
  width: 446px;
  height: 596px;
  box-sizing: border-box;
  border: 1px solid #E2E8F0;
  border-radius: 5px;
  background: #FFFFFF;
  box-shadow: 0 4px 12px 0 rgba(17,51,83,.02), 0 4px 12px 0 rgba(17,51,83,.02);
  h1{
    margin: 50px;
  }
}
</style>
