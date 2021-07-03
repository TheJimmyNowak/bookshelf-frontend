<template>
  <div id="content">
    <input name="book-search" placeholder="Czego szukasz?" v-model="searchedBook"/>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-info">
        <p class="book-title">Tytuł</p>
        <p>Bolszewicy</p>
      </div>
      <div class="buy-button">KUPUJ</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BookSearcher",
  data() {
    return {
      searchedBook: ""
    }
  }
}
</script>

<style scoped>
#content {
  width: 90vw;
  height: 100vh;
}
input {
  font-family: inherit;
  width: 50%;
  border: 0;
  border-bottom: 2px solid var(--clr-neutral-2);
  outline: 0;
  font-size: 1.3rem;
  color: var(--clr-neutral-2);
  padding: 7px 0;
  background: transparent;
  transition: border-color 0.2s;
  margin: 2vh;
}
.offer {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  background-color: var(--clr-primary-3);
}
.offer > img {
  padding: 1%;
  height: 40vh;
}
.book-info {
  text-align: left;
}
.buy-button {
  flex-grow: 12;
  text-align: right;
}
@media screen and (max-width: 768px) {
  .offer > img {
    width: 98%;
    height: 98%;
  }
}
</style>
