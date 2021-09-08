<template>
  <div class="box-card">
    <img :src="url" :alt="text" />
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: "Cards",
  data() {
    return {
      test: "test",
    };
  },
  props: ["text", "url"],
};
</script>

<style scoped lang="scss">
.box-card {
  flex-basis: 200px;
  padding: 20px;
  img {
    max-width: 100%;
  }
}
</style>