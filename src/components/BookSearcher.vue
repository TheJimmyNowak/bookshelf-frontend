<template>
  <div id="content">
    <input name="book-search" placeholder="Czego szukasz?" v-model="searchedBook"/>

    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
    </div>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
    </div>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
    </div>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
    </div>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
    </div>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
    </div>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
    </div>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
    </div>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
    </div>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
    </div>
    <div class="offer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
      <div class="book-data">
        <div class="book-info">
          <p class="book-title">Tytuł</p>
          <p>Bolszewicy</p>
        </div>
        <a href="/buy/" class="buy-button">
          <span>KUPUJ</span>
        </a>
      </div>
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
  width: 90%;
}


.offer {
  margin: 1rem;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  background-color: var(--clr-primary-3);
}

.book-data {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-grow: 12;
}

.offer > img {
  padding: 1%;
  height: 40vh;
}

.buy-button {
  width: 50%;
  margin-right: 1rem;
  background-color: var(--clr-primary-2);
  height: 3rem;
  vertical-align: middle;
}

.buy-button > span {
  display: inline-block;
  vertical-align: middle;
}

@media screen and (max-width: 768px) {
  .offer > img {
    width: 98%;
    height: 98%;
  }
}
</style>
