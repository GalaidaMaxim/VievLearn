<script>
import Container from "./Container.vue";
import ProductCard from "./ProductCard.vue";
import imagePath from "../assets/images/l2.png";
import imagePath2 from "../assets/images/l3.png";
import imagePath3 from "../assets/images/l4.png";

export default {
  data() {
    return {
      imagePath,
      imagePath2,
      imagePath3,
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
        <ProductCard
          :title="'Black Crop Tailored Jacket'"
          :price="'62.99'"
          :rating="'4.9'"
          :color="'#a9d4ba'"
          :imagePath="imagePath2"
        />
        <ProductCard
          :title="'Textured Sunset Shirt'"
          :price="'49.99'"
          :rating="'5.0'"
          :color="'#cadcd0'"
          :imagePath="imagePath3"
        />
        <!-- <img src="../assets/images/l2.png" alt="" /> -->
      </ul>
      <button>
        See all
        <svg class="arrow">
          <use href="../assets/images/Icons/sprite.svg#icon-arrow" />
        </svg>
      </button>
    </Container>
  </section>
</template>

<style scoped lang="scss">
@use "../assets/styles/functions" as *;
section {
  padding-top: 5.18rem;
  padding-bottom: rem(185px);
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
  gap: 2rem;
}

button {
  width: rem(224px);
  height: rem(65px);
  font-family: "Poppins";
  margin-top: rem(80px);
  display: flex;
  margin-left: auto;
  margin-right: auto;
  justify-content: center;
  gap: rem(18px);
  align-items: center;
  color: #224f34;
  border: 1px solid black;
  background-color: white;
  & .arrow {
    height: rem(30px);
    width: rem(23px);
    stroke: #224f34;
    fill: none;
  }
}
</style>
