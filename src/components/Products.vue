<script>
import i1 from "../assets/images/pl1.png";
import i2 from "../assets/images/pl2.png";
import i3 from "../assets/images/pl3.png";
import i4 from "../assets/images/pl4.png";
import i5 from "../assets/images/pl5.png";
import i6 from "../assets/images/pl6.png";
import i7 from "../assets/images/pl7.png";
import i8 from "../assets/images/pl8.png";

import Container from "./Container.vue";
import ProductCard from "./ProductCard.vue";
export default {
  data() {
    return {
      products: [
        {
          title: "Spread Collar Shirt",
          imagePath: i1,
          price: "48.99",
          rading: "5.0",
          imageLeftGap: "0px",
          imageRightGap: "0px",
        },
        {
          title: "White Solid Formal Shirt",
          imagePath: i2,
          price: "39.00",
          rading: "4.9",
          color: "#eaebf0",
        },
        {
          title: "Shine On Me Blouse",
          imagePath: i3,
          price: "42.99",
          rading: "4.8",
          color: "#eaebf0",
        },
        {
          title: "Gray Solid Padded Jacket",
          imagePath: i4,
          price: "32.99",
          rading: "4.7",
          color: "#eaebf0",
        },
        {
          title: "Printed Loose T-shirt",
          imagePath: i5,
          price: "39.99",
          rading: "5.0",
          color: "#eaebf0",
        },
        {
          title: "Summer Wind Crop Shirt",
          imagePath: i6,
          price: "39.95",
          rading: "4.7",
          color: "#eaebf0",
        },
        {
          title: "Tailored Jacket",
          imagePath: i7,
          price: "46.00",
          rading: "4.9",
          color: "#eaebf0",
        },
        {
          title: "Solid Round Neck T-shirt",
          imagePath: i8,
          price: "36.00",
          rading: "5.0",
          color: "#c2efd4",
        },
      ],
    };
  },
  components: {
    Container,
    ProductCard,
  },
};
</script>

<template>
  <Container class="container">
    <h2>Our products</h2>
    <ul class="control">
      <li>
        <button>Sale</button>
      </li>
      <li>
        <button>Hot</button>
      </li>
      <li>
        <button>New Arrivals</button>
      </li>
      <li>
        <button>Accessories</button>
      </li>
    </ul>
    <ul class="products">
      <ProductCard
        v-for="item in products"
        :price="item.price"
        :title="item.title"
        :rating="item.rading"
        :imagePath="item.imagePath"
        :imageRightGap="item.imageRightGap"
        :imageLeftGap="item.imageLeftGap"
        :color="item.color"
      />
    </ul>
  </Container>
</template>

<style scoped lang="scss">
@use "../assets/styles/functions" as *;
.container {
  text-align: center;
  // margin-top: rem(185px);
  margin-bottom: rem(195px);
}
h2 {
  font-size: rem(50px);
  color: #224f34;
  font-family: "Roboto Slab";
}
.control {
  margin-top: rem(70px);
  display: flex;
  justify-content: center;
  gap: rem(100px);
  & button {
    font-size: 1rem;
    text-transform: uppercase;
    border: none;
    background-color: transparent;
    padding: 0;
  }
}
.products {
  margin-top: rem(83px);
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  column-gap: rem(35px);
  row-gap: rem(85px);
}
</style>
