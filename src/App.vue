<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <p>Welcome</p>
  </div>

</template>

<script>

export default {
  name: 'app',
  components: {
  },
  data: function () {
    return {
      quotes: ['Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dignissimos, quidem!'],
      maxQuotes: 10
    }
  },
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
