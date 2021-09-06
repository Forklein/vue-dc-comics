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
        <div>
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
        <div>
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

#icons ul,
#icons li {
  display: flex;
  align-items: center;
  padding: 20px;
}

#icons img {
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
  justify-content: space-around;
  color: gray;
  font-size: 14px;
  background-image: url("../assets/img/footer-bg.jpg");
  background-size: cover;
}

#faq h3 {
  padding: 10px 0;
  color: #fff;
  font-size: 18px;
  text-transform: uppercase;
}

#faq .box {
  display: flex;
}

#faq div {
  margin: 0 50px;
}

#faq img {
  max-width: 50%;
}
</style>