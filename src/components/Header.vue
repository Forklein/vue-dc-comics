<template>
  <header>
    <div class="topbar">
      <img src="../assets/img/dc-logo.png" alt="Logo" />
      <nav>
        <ul>
          <li v-for="(link, index) in navbar" :key="index">
            <a :class="{ active: link.current }" :href="link.url">
              {{ link.text }}
            </a>
          </li>
        </ul>
      </nav>
    </div>
    <div class="jumbotron">
      <div class="current-series">Current Series</div>
    </div>
  </header>
</template>

<script>
import navbar from "../data/data";
export default {
  name: "Header",
  data() {
    return {
      test: "test",
      navbar,
    };
  },
  computed: {},
  methods: {},
  created() {},
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_mixins.scss";
@import "../assets/scss/_variable.scss";

header {
  .topbar {
    background-color: $color-white;
    padding: 10px;
    @include flex("evenly");
  }
  .jumbotron {
    height: 400px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
    position: relative;
  }
  .current-series {
    position: absolute;
    top: 95%;
    left: 20%;
    background-color: $color-jumbo;
    color: $color-white;
    padding: 10px;
    text-transform: uppercase;
  }
}

ul {
  @include flex;
  a {
    font-size: 13px;
    color: #000;
    text-transform: uppercase;
  }
}

.active {
  border-bottom: 1px solid $color-jumbo;
}
</style>