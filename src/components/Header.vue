<template>
  <header>
    <img src="../assets/img/dc-logo.png" alt="Logo" />
    <nav>
      <ul>
        <li v-for="(link, index) in navbar" :key="index">
          <a href="#">
            {{ link }}
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      Test: "test",
      navbar: [
        "Characters",
        "Comics",
        "Movies",
        "Tv",
        "Games",
        "Collectibles",
        "Videos",
        "Fans",
        "News",
        "Shop",
      ],
    };
  },
  computed: {},
  methods: {},
  created() {},
};
</script>

<style>
header {
  background-color: #fff;
  padding: 10px;
  margin-top: 20px;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
ul {
  display: flex;
}

a {
  font-size: 13px;
  color: #000;
  text-transform: uppercase;
}
</style>