<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
};
</script>

<style lang="scss">
@import "assets/scss/_mixins.scss";
@include reset;

body {
  background-color: #0e0e0e;
}

ul {
  list-style-type: none;
}

a {
  padding: 15px;
  text-decoration: none;
}
</style>
