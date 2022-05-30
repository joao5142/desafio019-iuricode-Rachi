<template>
  <header class="py-3 container">
    <nav class="d-flex justify-content-between nav-header">
      <img src="@/assets/images/logo.svg" alt="" />

      <ul class="d-flex nav-header__list">
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
  .nav-header__list {
    li {
      margin-left: 50px;
      color: $gray-color;
      font-weight: 500;
    }
  }
}
</style>
