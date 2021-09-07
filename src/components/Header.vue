<template>
  <header>
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
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      test: "test",
      navbar: [
        {
          text: "Characters",
          url: "#",
          current: false,
        },
        {
          text: "Comics",
          url: "#",
          current: true,
        },
        {
          text: "Movies",
          url: "#",
          current: false,
        },
        {
          text: "TV",
          url: "#",
          current: false,
        },
        {
          text: "Games",
          url: "#",
          current: false,
        },
        {
          text: "Collectibles",
          url: "#",
          current: false,
        },
        {
          text: "Videos",
          url: "#",
          current: false,
        },
        {
          text: "Fans",
          url: "#",
          current: false,
        },
        {
          text: "News",
          url: "#",
          current: false,
        },
        {
          text: "Shop",
          url: "#",
          current: false,
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
@import "@/assets/scss/_mixins.scss";
@import "@/assets/scss/_variable.scss";

header {
  background-color: $color-white;
  padding: 10px;
  margin-top: 20px;
  @include flex("evenly");
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