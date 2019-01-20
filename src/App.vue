<template>
  <div id="app">
    <Header v-on:profile="onProfileClick"></Header>
    <Main v-bind:profile-stat="see"></Main>
    <Footer></Footer>
  </div>
</template>

<script>

import Header from "./components/Header";
import Footer from "./components/Footer";
import Main from "./components/Main";

export default {
  name: 'app',
  data: () => {return{see: true}},
  methods: {
    onProfileClick: function (data) {
      this.see=data;
    }
  },
  components: {
    Main,
    Footer,
    Header
  }
}
</script>

<style lang="scss">
  body {
    margin: 0;
  }
  #app {
    display: flex;
    flex-direction: column;
    height: 100vh;

    @media screen and (min-width: 1200px) {
      width: 1200px;
      margin: 0 auto;
    }
}
</style>
