<template>
  <div class="container" id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <p>Welcome</p>
    <quote-grid :quotes="quotes"></quote-grid>
  </div>

</template>

<script>

import QuoteGrid from "./components/QuoteGrid/QuoteGrid";
export default {
  name: 'app',
  components: {
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
