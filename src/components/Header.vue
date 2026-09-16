<script>
import Container from "./Container.vue";
export default {
  components: { Container },
};
</script>

<template>
  <Container class="header-container">
    <p className="logo">Rivo</p>
    <nav>
      <a href="/">Home</a>
      <a href="/">Shop</a>
      <a href="/">Features</a>
      <a href="/">Contact</a>
    </nav>
    <button>Login</button>
  </Container>
</template>

<style scoped lang="scss">
.header-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
nav {
  display: flex;
}
.logo {
  font-family: Rufina;
  font-size: 1.8rem;
}
</style>
