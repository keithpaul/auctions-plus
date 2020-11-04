<template>
  <div class="form_container">
    <div class="form_contents">
        <div class="form_header_container">
            <h2 class="form_heading">Create Your Account</h2>
        </div>
        <form id="signupForm" class="user-form" @submit="checkForm" action="#" method="">
            <div class="input-area">
                <label for="firstName">First Name</label>
                <input class="form_input" id="firstName" v-model="firstName" type="text" name="firstName" placeholder="eg. John"/>
            </div>
            <div class="input-area">
                <label for="lastName">Last Name</label>
                <input class="form_input" id="lastName" v-model="lastName" type="text" name="lastName" placeholder="eg. Doe"/>
            </div>
            <div class="input-area">
                <label for="email">Email</label>
                <input class="form_input" id="email" v-model="email" type="email" name="firstName" placeholder="eg. John-Doe@gmail.com"/>
            </div>
            <div class="input-area">
                <label for="phone">Mobile or Landline with Area Code</label>
                <input class="form_input" id="phone" v-model="phone" type="text" name="phone" placeholder="eg. 041 123 4567"/>
            </div>
            <div class="input-area">
                <label for="phone">Password</label>
                <input class="form_input" id="password" v-model="password" type="password" name="password" placeholder=""/>
            </div>
            <div class="input-area-checkbox">                
                <input class="form_input" id="terms" v-model="readTerms" type="checkbox" name="terms" placeholder=""/>
                <p class="checkbox-label">I have read and agree to abide by the <a href="">AuctionsPlus User Agreement &amp; Sale Terms</a>.</p>
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
            signupDetails: {
                firstName: '',
                lastName: '',
                email: '',
                phone: '',
                password: '',
                readTerms: false
            }
        }
    }
}
</script>
