<script>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import BestSalis from "./components/BestSalis.vue";
import Products from "./components/Products.vue";
import Offer from "./components/Offer.vue";
import Designer from "./components/Designer.vue";
import Feedback from "./components/Feedback.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    Header,
    Hero,
    BestSalis,
    Products,
    Offer,
    Designer,
    Feedback,
    Footer,
  },
};
</script>

<template>
  <header>
    <Header />
  </header>
  <main>
    <Hero />
    <BestSalis />
    <Products />
    <Offer />
    <Designer />
    <Feedback />
  </main>
  <footer>
    <Footer />
  </footer>
</template>

<style scoped>
header {
  position: absolute;
  top: 0px;
  width: 100%;
  left: 0px;
}
footer {
  background-color: #224f34;
}
</style>
