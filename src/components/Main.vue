<template>
  <main>
    <section class="container" id="content">
      <Cards
        v-for="(comic, index) in comics"
        :key="index"
        :text="comic.series"
        :url="comic.thumb"
      />
    </section>
    <section id="icons">
      <ul>
        <li v-for="(icon, index) in icons" :key="index">
          <img :src="getImage(icon.image)" alt="icon" />
          <p>{{ icon.text }}</p>
        </li>
      </ul>
    </section>
    <section id="faq">
      <div class="box">
        <div>
          <h3>Dc Comics</h3>
          <ul>
            <li>Characters</li>
            <li>Comics</li>
            <li>Movies</li>
            <li>TV</li>
            <li>Games</li>
            <li>Videos</li>
            <li>News</li>
          </ul>
          <br /><br />
          <h3>Shop</h3>
          <ul>
            <li>Shop DC</li>
            <li>Shop DC Collectibles</li>
          </ul>
        </div>
        <div class="flex-start">
          <h3>DC</h3>
          <ul>
            <li>Terms of use</li>
            <li>Privacy Policy(new)</li>
            <li>Ad Choices</li>
            <li>Advertising</li>
            <li>Job</li>
            <li>Subscriptions</li>
            <li>Talent Workshops</li>
            <li>CPSC Certificates</li>
            <li>Rating</li>
            <li>Shop Help</li>
            <li>Contact Us</li>
          </ul>
        </div>
        <div class="flex-start">
          <h3>SITES</h3>
          <ul>
            <li>DC</li>
            <li>MAD Magazine</li>
            <li>DC Kids</li>
            <li>DC Universe</li>
            <li>DC Power Visa</li>
          </ul>
        </div>
      </div>
      <div class="img-box">
        <img src="../assets/img/dc-logo-bg.png" alt="" />
      </div>
    </section>
  </main>
</template>

<script>
import icons from "../data/icons.js";
import Cards from "../components/Cards.vue";
import comics from "../data/comics.js";

export default {
  name: "Main",
  data() {
    return {
      test: "test",
      icons,
      comics,
    };
  },
  components: {
    Cards,
  },
  computed: {},
  methods: {
    getImage(link) {
      return require(`@/assets/img/${link}`);
    },
  },
  created() {},
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_mixins.scss";
@import "../assets/scss/_variable.scss";

#content {
  color: $color-white;
  font-size: 12px;
  padding: 50px 0;
  @include flex;
  flex-wrap: wrap;
}

#icons {
  background-color: $color-jumbo;
  @include flex;
  ul {
    @include flex;
    padding: 20px;
    li {
      @include flex;
      padding: 20px;
      img {
        width: 50px;
      }
    }
    p {
      color: $color-white;
      margin-left: 20px;
    }
  }
}

#faq {
  @include flex("around");
  color: gray;
  font-size: 14px;
  padding: 20px;
  background-image: url("../assets/img/footer-bg.jpg");
  background-size: cover;
  h3 {
    padding: 10px 0;
    color: $color-white;
    font-size: 18px;
    text-transform: uppercase;
  }
  .box {
    @include flex;
  }
  div {
    margin: 0 50px;
  }
  img {
    max-width: 50%;
  }
  .flex-start {
    align-self: flex-start;
  }
}
</style>