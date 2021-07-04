<template>
  <div id="content">
    <form>
      <input v-model="email" placeholder="E-mail"/>
      <input v-model="username" placeholder="Nazwa użytkownika"/>
      <input v-model="password1" placeholder="Hasło" type="password"/>
      <input v-model="password2" placeholder="Potwierdź hasło" type="password">
      <a href="#" @click="submit">Dalej</a>
    </form>
    <span>{{ notification }}</span>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Register",
  data() {
    return {
      email: "",
      username: "",
      password1: "",
      password2: "",
      notification: ""
    }
  },
  methods: {
    submit() {
      if (this.username === "" || this.email === "" || this.password1 === "") {
        this.notification = "Uzupełnij wszystkie pola";
        return;
      }
      if (this.password2 !== this.password1) {
        this.notification = "Hasła muszą być takie same";
        return;
      }
      const requestContent = new FormData();
      requestContent.append("email", this.email);
      requestContent.append("name", this.username);
      requestContent.append("password", this.password1);

      axios.post("http://localhost:5000/api/register",
          requestContent,
          {
            "Content-Type":
                "multipart/form-data"
          }
      ).then((response) => {
        console.log(response);
        this.notification = "JD"
      }).catch((err) => {
        console.log(err);
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
