<template>
  <div id="content">
    <form>
      <input v-model="email" placeholder="E-mail"/>
      <input v-model="password" placeholder="Hasło" type="password"/>
      <a href="#" @click="submit">Dalej</a>
    </form>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Login",
  data() {
    return {
      email: "",
      password: "",
    }
  },
  methods: {
    submit() {
      const requestContent = new FormData();
      requestContent.append("email", this.email)
      requestContent.append("password", this.password)
      axios.post('http://localhost:5000/api/login',
          requestContent,
          {
            "Content-Type":
                "multipart/form-data"
          }
          ,
      ).then((response) => {
        localStorage.setItem('auth_token', response.data['token'])
      }).catch((error) => {
        console.log(error)
      })
    }
  }
}
</script>

<style scoped>
a {
  display: flex;
}
</style>
