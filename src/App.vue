<template>
  <div class="container" id="app">
    <div class="row">
      <div class="col-6 mx-auto">
        <div class="alert alert-info">Tap Quote to delete</div>
      </div>
    </div>

    <new-quote @quoteAdded="newQuote"></new-quote>
    <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>
  </div>

</template>

<script>

import QuoteGrid from "./components/QuoteGrid/QuoteGrid";
import NewQuote from "./components/NewQuote/NewQuote";
export default {
  name: 'app',
  components: {
    NewQuote,
    QuoteGrid
  },
  data: function () {
    return {
      quotes: ['Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dignissimos, quidem!',
               'Mattis Fermentum Ligula Purus Malesuada',
               'Donec ullamcorper nulla non metus auctor fringilla. Nullam quis risus eget urna mollis ornare vel eu leo. Integer posuere erat a ante venenatis dapibus posuere velit aliquet.'
      ],
      maxQuotes: 10
    }
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    },
    deleteQuote(index) { // VueJS passes arguement
      this.quotes.splice(index, 1);
    }
  }
}
</script>

<style lang="scss">
@import "~bootstrap/dist/css/bootstrap.min.css";

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
