<template>
    <div>
        <img src="https://www.testhr.pl/wp-content/uploads/2020/01/logo_1kolor.png"/>
        <div class="book-data">
          <div class="book-info">
            <p class="book-title"> {{name}} </p>
            <p> {{author}} </p>
          </div>
          <a v-bind:href="'/book/' + id" class="buy-button">
            <span>KUP</span>
          </a>
        </div>
    </div> 
</template>

<script>
export default {
  name: "Offer",
  props:['name', 'author', 'id']
  
}
</script>

<style scoped>

</style>
