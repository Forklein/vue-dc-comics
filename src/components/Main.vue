<template>
  <main>
    <section id="content">Content goes here</section>
    <section id="icons">
      <ul>
        <li v-for="(icon, index) in icons" :key="index">
          <img :src="`../assets/img/${icon.image}`" alt="icon" />
          <p>{{ icon.text }}</p>
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