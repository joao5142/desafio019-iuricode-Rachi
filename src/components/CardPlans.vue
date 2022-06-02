<template>
  <div
    class="card-plans d-flex flex-column align-items-center"
    :class="{ 'card-plans--dark': preferred }"
  >
    <p class="card-plans__type">{{ type }}</p>
    <button class="card-plans__button-preferred" v-if="preferred">
      PREFERIDO
    </button>
    <p class="card-plans__money-container mt-3">
      <span class="card-plans__symbol-real">R$</span>
      <span class="card-plans__price">{{ price }}</span
      >/mês
    </p>
    <p class="card-plans__description mb-5">
      {{ description }}
    </p>

    <button class="card-plans__button">Assinar</button>
  </div>
</template>

<script>
export default {
  name: "CardPlans",
  props: {
    type: String,
    price: Number,
    description: String,
    preferred: Boolean,
  },
};
</script>

<style scoped lang="scss">
%button-default {
  background-color: $blue-color;
  color: $white-color;
  box-shadow: 1px 3px 4px rgba(19, 125, 224, 0.5);
}

.card-plans {
  padding: 50px 35px;
  border-radius: 8px;
  background-color: $white-200-color;
  min-height: 420px;

  &__type {
    font-size: 1.5rem;
    font-weight: 600;
  }

  &__money-container {
    font-weight: 800;
    font-size: 1.3rem;
    position: relative;

    .card-plans__symbol-real {
      font-size: 0.9rem;
      position: absolute;
      top: 10px;
      left: -20px;
      font-family: "Roboto", sans-serif;
    }
    .card-plans__price {
      font-size: 2.5rem;
      font-family: "Roboto", sans-serif;
    }
  }

  &__description {
    color: $gray-color;
    font-size: 1.1rem;
    text-align: center;
  }
  &__button {
    @extend %button-default;
    border-radius: 50px;
    padding: 8px 70px;
  }

  &__button-preferred {
    @extend %button-default;
    font-size: 0.8rem;
    padding: 4px 32px;
    border-radius: 20px;
  }
}

.card-plans--dark {
  background-color: $gray-200-color;
  color: $white-color;
  padding-top: 23px;

  & .card-plans__description {
    color: $gray-light-color;
  }
}
</style>