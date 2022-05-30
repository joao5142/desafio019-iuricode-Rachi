<template>
  <main class="container">
    <section class="row section-working mt-4">
      <div
        class="col-md-6 d-flex flex-column align-items-start justify-content-center"
      >
        <p class="section-working__title">
          Rachi, é tudo que você precisa em um só lugar.
        </p>
        <button class="mt-5 section-working__btn-cadastrar">
          Cadastrar-se
        </button>
      </div>

      <div class="col-md-6 d-flex justify-content-center">
        <img src="@/assets/images/working.svg" alt="" />
      </div>
    </section>

    <section class="section-how-it-works mt-5">
      <p class="--title-default text-center">Como funciona</p>
    </section>
  </main>
</template>

<script>
export default {
  name: "Main",
};
</script>

<style scoped lang="scss">
%btn-blue {
  background-color: $blue-color;
  color: $white-color;
  box-shadow: 1px 3px 4px rgba(19, 125, 224, 0.5);
  border-radius: 50px;
}
.--title-default {
  font-family: "Sora", sans-serif;
  font-size: 2.5rem;
}

.section-working {
  .section-working__title {
    font-size: 3rem;
    font-weight: 600;
    color: $gray-200-color;
  }
  .section-working__btn-cadastrar {
    @extend %btn-blue;
    padding: 10px 30px;
    font-weight: 600;
  }
}
.section-how-it-works {
}
</style>
