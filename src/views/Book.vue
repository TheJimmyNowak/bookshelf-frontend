<template>
  <div>
    <h1>{{bookTitle}}</h1>
    <h2>{{bookAuthor}}</h2>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Book",
  data() {
    return {
      id: this.$route.params.id,
      bookTitle: "",
      bookAuthor: "",
    }
  },
  methods: {
    fetchBook() {
      axios.get("http://localhost:5000/api/book/" + this.id)
          .then((response) => {
            this.bookTitle = response.data.name;
            this.bookAuthor = response.data.author;
          })
    }
  },
  mounted() {
    this.fetchBook();
  }
}
</script>

<style scoped>

</style>
