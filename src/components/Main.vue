<template>
  <main>
    <section id="content">Content goes here</section>
    <section id="icons">
      <ul>
        <li v-for="(icon, index) in icons" :key="index">
          <img :src="getImgUrl(icon.image)" alt="icon" />
          <p>{{ icon.text }}</p>
        </li>
      </ul>
    </section>
    <section id="faq">
      <div class="box">
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
      <div class="box">
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
      <div class="box">
        <h3>SITES</h3>
        <ul>
          <li>DC</li>
          <li>MAD Magazine</li>
          <li>DC Kids</li>
          <li>DC Universe</li>
          <li>DC Power Visa</li>
        </ul>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "Main",
  data() {
    return {
      test: "test",
      icons: [
        {
          image: "buy-comics-digital-comics.png",
          text: "DIGITAL COMICS",
        },
        {
          image: "buy-comics-merchandise.png",
          text: "DC MERCHANDISE",
        },
        {
          image: "buy-comics-subscriptions.png",
          text: "SUBSCRIPTION",
        },
        {
          image: "buy-comics-shop-locator.png",
          text: "COMIC SHOP LOCATOR",
        },
        {
          image: "buy-dc-power-visa.svg",
          text: "DC POWER VISA",
        },
      ],
    };
  },
  computed: {},
  methods: {
    getImgUrl(pic) {
      return require(`@/assets/img/${pic}`);
    },
  },
  created() {},
};
</script>

<style scoped lang="scss">
$color-jumbo: #0282f9;

ul,
li {
  display: flex;
  align-items: center;
  padding: 20px;
}

img {
  width: 50px;
}

#content {
  color: #fff;
  font-size: 36px;
  padding: 50px 350px;
}

#icons {
  background-color: $color-jumbo;
  display: flex;
  justify-content: center;
}

#faq {
  display: flex;
  padding: 50px 350px;
  color: gray;
  font-size: 14px;
  background-image: url("../assets/img/footer-bg.jpg");
  background-size: contain;
}

#faq ul {
  display: block;
  padding: 0;
}

#faq li {
  display: block;
  padding: 0;
}

#faq h3 {
  padding: 10px 0;
  color: #fff;
  font-size: 18px;
  text-transform: uppercase;
}

#faq .box {
  margin: 20px;
}
</style>