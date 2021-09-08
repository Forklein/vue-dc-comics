<template>
  <div class="box-card">
    <div class="img-card">
      <img :src="url" :alt="text" />
    </div>
    <div class="text-card">
      <p>{{ text }}</p>
    </div>
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
  height: 300px;
  .img-card {
    padding: 20px;
    img {
      max-width: 100%;
    }
  }
  .text-card {
    padding: 0 20px;
  }
}
</style>