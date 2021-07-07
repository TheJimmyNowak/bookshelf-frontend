<template>
  <div id="content">
    <input name="book-search" placeholder="Czego szukasz?" v-model="searchedBook" @input="search"/>

    <transition-group name="book-list">
      <div class="offer" v-for="book in books" :key="book._id">
        <img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Mein_Kampf_dust_jacket.jpeg"/>
        <div class="book-data">
          <div class="book-info">
            <p class="book-title">{{ book.name }}</p>
            <p>{{ book.author }}</p>
          </div>
          <a href="/book/" class="buy-button">
            <span>KUPUJ</span>
          </a>
        </div>
      </div>
    </transition-group>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "BookSearcher",
  data() {
    return {
      searchedBook: "",
      books: []
    }
  },
  methods: {
    search() {
      axios.get("http://localhost:5000/api/book/filter?name=" + this.searchedBook)
          .then((res) => {
            this.books = res.data
            console.log(res)
          })
          .catch((err) => {
            console.log(err)
          })
    }
  },
  mounted() {
    this.search()
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

.book-list-enter-active, .book-list-leave-active {
  transition: all 1s;
}

.book-list-enter, .book-list-leave-to {
  opacity: 0;
  transform: scale(0.9);
}

@media screen and (max-width: 768px) {
  .offer > img {
    width: 98%;
    height: 98%;
  }
}
</style>
