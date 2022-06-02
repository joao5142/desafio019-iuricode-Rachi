<template>
  <div
    class="
      d-flex
      justify-center
      align-items-center
      flex-column
      card-how-it-works
    "
  >
    <img
      class="card-how-it-works__image mb-2"
      :src="getImgUrl(image)"
      alt="Conexões"
    />
    <p class="card-how-it-works__title mb-2">{{ title }}</p>
    <p class="card-how-it-works__description">{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: "HowWorkCard",
  props: {
    image: String,
    title: String,
    description: String,
  },
  methods: {
    getImgUrl(values) {
      var images = require.context("@/assets/images", false);
      return images("./" + values);
    },
  },
};
</script>

<style scoped lang="scss">
.card-how-it-works {
  font-family: "Sora", sans-serif;
  .card-how-it-works__image {
    width: 70px;
    height: 70px;
  }
  .card-how-it-works__title {
    font-weight: 600;
  }
  .card-how-it-works__description {
    font-family: "Inter";
    font-size: 1.1rem;
    text-align: center;
    color: $gray-color;
  }
}
</style>