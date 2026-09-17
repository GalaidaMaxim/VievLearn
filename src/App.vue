<script>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import BestSalis from "./components/BestSalis.vue";
export default {
  components: { Header, Hero, BestSalis },
};
</script>

<template>
  <header>
    <Header />
  </header>
  <main>
    <Hero />
    <BestSalis />
  </main>
  <footer></footer>
</template>

<style scoped>
header {
  position: absolute;
  top: 0px;
  width: 100%;
  left: 0px;
}
</style>
