<template lang="">
    <v-container>
        <v-row justify="center">
            <h1>Login Page Welcome</h1>
        </v-row>
        <v-row>
            <v-col>
                <v-form>
                    <label >Enter Your Email</label>
                    <v-text-field
                        v-model="formData.email"
                        name="email"
                        required
                    ></v-text-field>
                    <label >Enter Your password</label>
                    <v-text-field
                        v-model="formData.password"
                        required
                    ></v-text-field>


                    <v-btn @click="HandleSubmit()">
                        Submit
                    </v-btn>
                </v-form>
                <v-row style="margin-top:50px;">
                    <div v-if="tempData.email.length>0 && tempData.password.length>0">
                        <b>
                            Email Address is: {{ tempData.email }}
                        </b>
                        <br/>
                        <b>
                            password is: {{ tempData.password }}
                        </b>
                    </div>
                </v-row>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name:"LoginPage",

    data() {
       return {
        formData:{
            email:"",
            password:"",
        },
        tempData:{
            email:"",
            password:""
        }
       }
    },

    methods: {
        async HandleSubmit() {
            this.tempData.email = this.formData.email;
            this.tempData.password = this.formData.password;
            this.formData.email = "";
            this.formData.password = "";
        }
    }
};
</script>