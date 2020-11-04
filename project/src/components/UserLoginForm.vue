<template>
  <div class="form_container">
    <div class="form_contents">
        <div class="form_header_container">
            <h2 class="form_heading">Log In</h2>
        </div>
        <form id="loginForm" class="user-form" @submit="checkForm" action="#" method="">
            <div class="input-area">
                <label for="email">Email</label>
                <input class="form_input" id="email" v-model="email" type="email" name="firstName" placeholder="eg. John-Doe@gmail.com"/>
            </div>
            <div class="input-area">
                <label for="phone">Password</label>
                <input class="form_input" id="password" v-model="password" type="password" name="password" placeholder=""/>
            </div>
            <div class="forgot-password">
                <p class="forgot-password-text"><a href="">Forgot your Password? Click here.</a></p>
            </div>
            <div class="input-area-submit">
                <input class="form_submit" type="submit" value="Submit" >
            </div>
        </form>
    </div>
  </div>
</template>

<script>
export default {
    name: 'UserSignupForm',
    props: {
        msg: String
    },
    data(){
        return {
            loginDetails: {
                email: '',
                password: '',
            }
        }
    }
}
</script>
