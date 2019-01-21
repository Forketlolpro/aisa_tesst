<template>
  <div id="app">
    <Header @showm="showModal = true" v-on:profile="onProfileClick"></Header>
    <Main @showm="showModal = true" v-bind:profile-stat="see"></Main>
    <Footer></Footer>
    <Modal v-if="showModal"  @close="showModal = false"></Modal>
  </div>
</template>

<script>

import Header from "./components/Header";
import Footer from "./components/Footer";
import Main from "./components/Main";
import Modal from "./components/Modal";

export default {
  name: 'app',
  data: () => {return{see: true,showModal: false}},
  methods: {
    onProfileClick: function (data) {
      this.see=data;
    }
  },
  components: {
    Modal,
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
    min-height: 100vh;

    @media screen and (min-width: 1200px) {
      width: 1200px;
      margin: 0 auto;
    }
}
</style>
