<template>

    <form id="signup-form">
   
        
       
        <div class="row">
           
                <h1>Sign Up</h1>
                
        

           
            <div class="col-12 form-group">
                <label class="col-form-label col-form-label-lg">First name<span class="text-danger"></span></label>
                <input type="text" class="form-control form-control-lg" placeholder="Firstname" v-model="firstName" :class="{'is-invalid': !isFirstNameValid}">
                <div class="invalid-feedback" v-if="!isFirstNameValid">Please enter your first name.</div>
            </div>
            <div class="col-12 form-group">
                <label class="col-form-label col-form-label-lg">Last name<span class="text-danger"></span></label>
                <input type="text" class="form-control form-control-lg" placeholder="Lastname" v-model="lastName" :class="{'is-invalid': !isLastNameValid}">
                <div class="invalid-feedback" v-if="!isLastNameValid">Please enter your last name.</div>
            </div>
            <div class="col-12 form-group">
                <label class="col-form-label col-form-label-lg">Email address<span class="text-danger"></span></label>
                <input type="email" class="form-control form-control-lg" placeholder="Enter Your Email" id="email" v-model="email" :class="{'is-invalid': !isEmailValid}">
                <div class="invalid-feedback" v-if="!isEmailValid">Please enter a valid email address.</div>
            </div>
            <div class="col-12 form-group">
                <label class="col-form-label col-form-label-lg"> Password<span class="text-danger"></span></label>
                <input type="password" class="form-control form-control-lg" placeholder="Enter your password" id="password" v-model="password" :class="{'is-invalid': !isPasswordValid}">
                <div class="invalid-feedback" v-if="!isPasswordValid">Please enter a password with at least 8 characters, upper case,lower case and a number</div>
            </div>
            <div class="col-12 form-group text-center">
                <button type="text" class="form-control form-control-g" >SIGN UP</button>
             <p>Already registered <a href="#">sign in?</a></p>
            </div>  
        </div>
    </form>
</template>
<script>

export default{
            data() {
                return {
                    name: '',
                    firstName: '',
                    lastName: '',
                    email: '',
                    password: '',
                }
            },
            computed: {
                isNameValid() {
                    return this.name.trim() !== '';
                },
                isFirstNameValid() {
                    return this.firstName.trim() !== '';
                },
                isLastNameValid() {
                    return this.lastName.trim() !== '';
                },
                isEmailValid() {
                    const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                    return emailPattern.test(this.email.trim());
                },
                isPasswordValid() {
                    const passwordPattern= /^(?=.*[A-Z])(?=.*\d)(?=.*[!@#$%^&*()_+])[A-Za-z\d!@#$%^&*()_+]{8,}$/;
                    passwordPattern.length >= 8;
                    return passwordPattern.test(this.password.trim());
                },
                isFormValid() {
                    return this.isNameValid && this.isFirstNameValid && this.isLastNameValid && this.isEmailValid && this.isPasswordValid;
                },
            },
            methods: {
                submitForm() {
                    if (this.isFormValid) {
                        alert('Form submitted successfully!');
                        // You can add more code to handle form submission here.
                    }
                },
            },
        };



</script>
<style>
.row{
    
    text-align: left; 
    
    
    
}
h1{
    margin-left: 170px;
    margin-top: 20px;
    font-weight: bold;
}

.form-control-g{
    background-color: blue;
    color:aliceblue;
}
p{
    margin-left: 200px;
    font-weight: 200;
}

</style>
