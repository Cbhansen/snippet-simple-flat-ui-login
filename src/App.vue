<template>
  <div id="app">
    <div id="formContainer">
      <form v-on:submit.prevent="submitForm()" id="form">
        <input v-model="credentials.id" type="text" placeholder="Username">
        <input v-model="credentials.secret" type="password" placeholder="Password">
        <p><button id="loginBtn">Login</button></p>
        <p>Not registered? <a href="#">Create an account!</a></p>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      title: 'Generic Login Page',
      credentials: {
        id: '',
        secret: null
      }
    }
  },
  methods: {
    submitForm() {
      
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background: linear-gradient(to right,#b4e4ab, #82df8a);
}

#formContainer {
  text-align: center;
  width: auto;
  height: auto;
  min-height: 350px;
  max-width: 500px;
  min-width: auto;
  margin: 100px auto;
  background: #eee;
  box-shadow: 2px 5px 10px#333;
  transition: .3s all;
    &:hover {
      box-shadow: 1px 3px 5px #333;
    }
}
form {
  padding: 70px;
}
input {
  border: none;
  outline: none;
  padding: 10px;
  &:focus {
    outline: none;
  }
}
input[type=text]::placeholder,
input[type=password]::placeholder {

}
input[type=text],
input[type=password] {
  font-size: 20px;
  margin: 5px;
}

#loginBtn {
  width: 230px;
  background: orange;
  outline: none;
  border: none;
  font-size: 20px;
  padding: 10px;
  transition: .3s all;
  cursor: pointer;
    &:focus {
      outline: none;
    }
    &:hover {
      background: #b4e4ab;
    }
}

a {
  color: #42b983;
  text-decoration: none;
    &:hover {
      text-decoration: underline;
      color: orange;
    }
}
</style>
