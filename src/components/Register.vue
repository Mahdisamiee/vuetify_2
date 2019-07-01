<template>
    <v-dialog max-width="500px" v-model="dialog" persistent >
        <v-btn slot="activator" small flat class="white grey--text">
            <span>ثبت نام</span>
            <v-icon small left>input</v-icon>
        </v-btn>
        <v-card>
            <v-layout column justify-center align-center>
                <v-flex xs12 class="mt-4">
                    <v-avatar
                        size="80"
                        class=""
                    >
                        <img src="https://cdn3.iconfinder.com/data/icons/stroke/53/Smile-512.png" alt="alt">
                    </v-avatar>
                </v-flex>
                <v-flex xs12>
                    <v-card-title primary-title>
                        <h3>ورود</h3>
                    </v-card-title>
                </v-flex>
            </v-layout>
            <v-card-text>
                <v-form class="pa-4">
                    <v-text-field v-model="fname" label="نام" prepend-icon="face"></v-text-field>
                    <v-text-field v-model="lname" label="نام خانوادگی" prepend-icon="person"></v-text-field>
                    <v-text-field
                        label="E-mail"
                        v-model="email"
                        :rules="[rules.required, rules.email]"
                        prepend-icon="email"
                    ></v-text-field>
                    <v-text-field
                        v-model="password"
                        :append-icon="show ? 'visibility' : 'visibility_off'"
                        :rules="[rules.required, rules.min]"
                        :type="show ? 'text' : 'password'"
                        label="رمز عبور"
                        hint="At least 8 characters"
                        counter
                        @click:append="show = !show"
                        prepend-icon="https"
                    ></v-text-field>
                    <v-spacer></v-spacer>
                    <v-btn depressed small class="success mt-3 mb-0 ml-0" @click="submit" >تائید</v-btn>
                </v-form>
            </v-card-text>
        </v-card>
    </v-dialog>
</template>

<script>
export default {
    data(){
        return{
            dialog:false,
            fname:'',
            lname:'',
            email:'',
            show:false,
            password:'',
            rules: {
                required: value => !!value || 'Required.',
                counter: value => value.length <= 20 || 'Max 20 characters',
                min: v => v.length >= 8 || 'Min 8 characters',
                email: value => {
                    const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
                    return pattern.test(value) || 'Invalid e-mail.'
                },
            },
            
        }
    },
    methods:{
        submit(){
            this.dialog = false
        }
    }
}
</script>

<style>

</style>
