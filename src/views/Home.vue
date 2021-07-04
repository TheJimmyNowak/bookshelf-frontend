<template>
  <div id="container">
    <header>
      <div class="stats">
        <h1>57</h1>
        <b>Kupionych książek</b>
      </div>
      <div class="stats">
        <h1>57</h1>
        <b>Szczęśliwych użytkowników</b>
      </div>
      <div id="login-buttons">
        <a class="button" href="/login" style="background-color: #5998C5">
          Zaloguj
        </a>
        <a class="button" href="/register" style="background-color: #1B998B">
          Zarejestruj się
        </a>
      </div>
    </header>
    <BookSearcher/>
  </div>
</template>

<script>

import BookSearcher from "@/components/BookSearcher";

export default {
  components: {BookSearcher}
}
</script>

<style>
header,
#container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.stats {
  position: relative;
  padding: 5vw;
  max-width: 15vw;
}

#login-buttons {
  display: flex;
  flex-direction: column;
  padding: 5vw;
  column-gap: 5px;
}

.button {
  width: 15vw;
  height: 5vh;
  margin-top: 1vh;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 3vw;
  transition: all .2s ease-in-out;
}

.button:hover {
  transform: scale(0.9);
}

@media screen and (max-width: 768px) {
  .stats {
    display: none;
  }

  .button {
    width: 40vw;
  }
}
</style>
