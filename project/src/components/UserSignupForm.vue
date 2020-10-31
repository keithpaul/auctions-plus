<template>
  <div class="signup-form_container">
    <div class="signup-form_contents">
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
                <p class="checkbox-label" for="terms">I have read and agree to abide by the <a href="">AuctionsPlus User Agreement &amp; Sale Terms</a>.</p>
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.signup-form_container{
    width: 100%;
    height: 100%;
    .signup-form_contents{
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
            .input-area-checkbox{
                padding: 8px 36px;
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
                }
            }
            
        }
    }
}

</style>
