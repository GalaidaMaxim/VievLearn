<script>
import Container from "./Container.vue";
import ProductCard from "./ProductCard.vue";
import imagePath from "../assets/images/l2.png";
export default {
  data() {
    return {
      imagePath,
    };
  },
  components: {
    Container,
    ProductCard,
  },
};
</script>

<template>
  <section>
    <Container class="container">
      <h2>Best selling</h2>
      <p class="subtitle">
        Get in on the trend with our curated selection of best-selling styles.
      </p>
      <ul>
        <ProductCard
          :title="'Regular Fit Long Sleeve Top'"
          :price="'38.99'"
          :rating="'5.0'"
          :color="'#93b9a2'"
          :imagePath="imagePath"
        />
        <!-- <img src="../assets/images/l2.png" alt="" /> -->
      </ul>
    </Container>
  </section>
</template>

<style scoped>
section {
  padding-top: 5.18rem;
}
.container {
  text-align: center;
}

h2 {
  font-size: 2.9rem;
  font-family: "Roboto Slab";
  font-weight: 500;
  color: #224f34;
}

.subtitle {
  margin-top: 1.63rem;
  font-family: "Poppins";
  color: #224f34;
}

ul {
  margin-top: 3.63rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
</style>
