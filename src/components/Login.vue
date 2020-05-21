<template>
    <div id="login">
        <h1>Login</h1>
        <input type="text" name="username" v-model="input.username" placeholder="Username" />
        <input type="password" name="password" v-model="input.password" placeholder="Password" />
        <button type="button" v-on:click="login()">Login</button>
    </div>
</template>

<script>
    export default {
        name: 'Login',
        data() {
            return {
                input: {
                    username: "",
                    password: ""
                }
            }
        },
        methods: {
            login() {
                if(this.input.username != "" && this.input.password != "") {
                     console.log("A username and password must be present")
                } else {
                    console.log("A username and password must be present");
                }
            }
        }
    }
</script>

<style scoped>
    #login {
  width: 500px;
  border: 1px solid #CCCCCC;
  background-color: #FFFFFF;
  width: 350px;
  height: 350px;
  background: gray;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  border-right: 2px solid white;
  
    }
</style>