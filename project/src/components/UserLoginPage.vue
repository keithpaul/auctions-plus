<template>
  <div class="btn-group">
    <button class="btn btn-signup" @click="signup = false">Log In</button>
    <button class="btn btn-login" @click="signup = true">Sign Up</button>
  </div>
  <div class="login-form_container">
    
    
    <UserSignupForm v-if="signup == true"/>
    <UserLoginForm v-if="signup == false"/>
  </div>
</template>

<script>
import UserSignupForm from '@/components/UserSignupForm'
import UserLoginForm from '@/components/UserLoginForm'

export default {
  components: {
    UserSignupForm,
    UserLoginForm
  },
  name: 'UserLoginPage',
  props: {
    msg: String
  },
  data(){
    return{
      signup: true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.btn-group{
  width: 150px;
  height: 35px;
  display: flex;
  justify-content: space-between;
  position: fixed;
  top: 10px;
  right: 20px;
  .btn{
    height: 35px;
    width: 70px;
    border: 1px solid #ccc;
    border-radius: 5px;
    outline: none;
    cursor: pointer;
    &.btn-login{
      background: rgb(131, 131, 255);
      border: 1px solid rgb(131, 131, 255);
      color: white;
    }
    &.btn-signup{
      background: rgb(255, 247, 131);
      border: 1px solid rgb(255, 247, 131);
    }
  }
}
.login-form_container{
  margin: 40px 0;
  box-sizing: border-box;
  border: 1px solid #E2E8F0;
  border-radius: 5px;
  background: #FFFFFF;
  box-shadow: 0 4px 12px 0 rgba(17,51,83,.02), 0 4px 12px 0 rgba(17,51,83,.02);
  h1{
    margin: 50px;
  }
}

.form_container{
    width: 100%;
    height: 100%;
    .form_contents{
        width: 100%;
        height: 100%;
        box-sizing: border-box;
        .form_header_container{
            width: 100%;
            padding: 16px;
            box-sizing: border-box;
            border-bottom: 1px solid #E2E8F0;
            .form_heading{
                font-size: 20px;
                line-height: 30px;
                color: #002341;
                text-align: left;
                font-style: normal;
                font-weight: normal;
            }
        }
        .user-form{
            width: 100%;
            height: 100%;
            box-sizing: border-box;
            padding-top: 8px;
            .input-area{
                display: flex;
                flex-direction: column;
                padding: 8px 36px;
                label{
                    flex: 0 0 100%;
                    font-style: normal;
                    font-weight: normal;
                    font-size: 16px;
                    line-height: 24px;
                    color: #002341;
                }
                input[type='text'],input[type='email'],input[type='password']{
                    flex: 0 0 100%;
                    font-size: 12px;
                    line-height: 24px;
                    background: #FFFFFF;
                    border: 1px solid #E2E8F0;
                    box-sizing: border-box;
                    border-radius: 5px;
                    display: block;
                    padding: 7px 12px;
                    ::placeholder {
                        color: #A7A7A7;
                        opacity: 1; /* Firefox */
                    }
                    :-ms-input-placeholder { /* Internet Explorer 10-11 */
                        color: #A7A7A7;
                    }
                    ::-ms-input-placeholder { /* Microsoft Edge */
                        color: #A7A7A7;
                    }
                }
                
            }
            .forgot-password{
                padding: 4px 36px 18px 36px;
                .forgot-password-text{
                    font-style: normal;
                    font-weight: normal;
                    font-size: 14px;
                    line-height: 24px;
                    color: #002341;
                    a{
                        color: #008CD2;
                        text-decoration: none;
                    }
                }
            }
            .input-area-checkbox{
                padding: 4px 36px 18px 36px;
                display: flex;
                flex-direction: row;
                input[type='checkbox']{
                    flex: 0 0 16px;
                    border: 1px solid #E2E8F0;
                    box-sizing: border-box;
                    height: 16px;
                    width: 16px;
                    border-radius: 0;
                    margin-top: 4px;
                    margin-right: 12px;
                }
                .checkbox-label{
                    font-style: normal;
                    font-weight: normal;
                    font-size: 14px;
                    line-height: 24px;
                    color: #002341;
                    a{
                        color: #008CD2;
                        text-decoration: none;
                    }
                }
            }
            .input-area-submit{
                width: 100%;
                box-sizing: border-box;
                border-top: 1px solid #E2E8F0;
                padding: 12px 16px;
                .form_submit{
                    width: 92px;
                    height: 40px;
                    background: #002341;
                    border-radius: 5px;  
                    font-style: normal;
                    font-weight: normal;
                    font-size: 18px;
                    line-height: 24px;  
                    color: #ffffff;  
                    cursor: pointer;   
                }
            }
            
        }
    }
}

@media only screen and (min-width: 768px){
  .login-form_container{
    width: 446px;
  }
}
@media only screen and (max-width: 767px){
  .login-form_container{
    width: 350px;
  }
}
@media only screen and (max-width: 320px){
  .login-form_container{
    width: 300px;
  }
}
</style>
