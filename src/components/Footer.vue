<template>
  <footer>
    <section>
      <h3>Sign-Up Now!</h3>
    </section>
    <section id="icons">
      <div class="text">
        <p>Follow Us</p>
      </div>
      <div class="box-img">
        <img src="../assets/img/footer-facebook.png" />
        <img src="../assets/img/footer-twitter.png" />
        <img src="../assets/img/footer-youtube.png" />
        <img src="../assets/img/footer-pinterest.png" />
        <img src="../assets/img/footer-periscope.png" />
      </div>
    </section>
  </footer>
</template>

<script>
export default {
  name: "Footer",
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
@import "@/assets/scss/_mixins.scss";
@import "@/assets/scss/_variable.scss";

footer {
  @include flex("evenly");
  background-color: #303030;
  padding: 20px;
}

section:first-child {
  color: $color-white;
  border: 1px solid $color-jumbo;
  padding: 20px;
  text-transform: uppercase;
}

img {
  margin: 0 15px;
}

#icons {
  @include flex;
  color: $color-jumbo;
  text-transform: uppercase;
}
</style>