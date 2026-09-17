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
  padding-top: 2.45rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
nav {
  display: flex;
  gap: 2.36rem;
  & a {
    color: #224f34;
    text-decoration: none;
    font-family: Poppins;
    text-transform: uppercase;
  }
}
.logo {
  font-family: Rufina;
  font-size: 1.8rem;
  color: #224f34;
}
button {
  border: 1px solid #224f34;
  color: #224f34;
  font-family: Poppins;
  text-transform: uppercase;

  background-color: transparent;
  width: 6.45rem;
  height: 2.36rem;
  border-radius: 3px;
}
</style>
