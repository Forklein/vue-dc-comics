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
footer {
  background-color: #303030;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  padding: 20px;
}

section:first-child {
  color: #fff;
  border: 1px solid #0282f9;
  padding: 20px;
  text-transform: uppercase;
}

img {
  margin: 0 15px;
}

#icons {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #0282f9;
  text-transform: uppercase;
}
</style>