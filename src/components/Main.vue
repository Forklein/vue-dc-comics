<template>
  <main>
    <section id="content">Content goes here</section>
    <section id="icons">
      <ul>
        <li>
          <img src="../assets/img/buy-comics-digital-comics.png" alt="icon" />
          <p>Test</p>
        </li>
      </ul>
    </section>
  </main>
</template>

<script>
export default {
  name: "Main",
  data() {
    return {
      test: "test",
    };
  },
  computed: {},
  methods: {},
  created() {},
};
</script>

<style scoped lang="scss">
$color-jumbo: #0282f9;

#content {
  color: #fff;
  font-size: 36px;
  padding: 50px 350px;
}

ul,
li {
  display: flex;
  align-items: center;
  padding: 20px;
}

#icons {
  background-color: $color-jumbo;
  display: flex;
  justify-content: center;
}

img {
  width: 50px;
}
</style>