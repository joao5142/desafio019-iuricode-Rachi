<template>
  <header class="py-3 container">
    <nav class="d-flex flex-wrap justify-content-between nav-header">
      <img src="@/assets/images/logo.svg" alt="" class="mt-3 me-5" />

      <ul class="d-flex nav-header__list mt-3">
        <li>Funcionalidades</li>
        <li>App</li>
        <li>Planos</li>
        <li>Contato</li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped lang="scss">
.nav-header {
  &__list {
    padding-left: 0px;
    margin-bottom: 0px;
    justify-content: end;
    align-items: center;
    flex: 1;

    li {
      color: $gray-color;
      font-weight: 500;
      position: relative;

      &::after {
        transition: all 0.7 ease-in-out;
        transform-origin: left;
      }
      &:hover::after {
        content: "";
        position: absolute;
        left: 0px;
        bottom: -5px;
        height: 3px;
        width: 100%;
        border-radius: 3px;
        background-color: $blue-color;
        animation: fullWidthLine 0.7s ease-in-out;
      }
    }

    @keyframes fullWidthLine {
      0% {
        width: 0px;
      }
      100% {
        width: 100%;
      }
    }

    li:not(li:nth-child(1)) {
      margin-left: 50px;
    }

    @media (max-width: 450px) {
      li:not(li:nth-child(1)) {
        margin-left: 10px;
      }
    }
    @media (max-width: 767px) {
      & {
        justify-content: center;
      }
    }
  }
}
</style>
