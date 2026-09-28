<script>
import Container from "./Container.vue";
import ProductCard from "./ProductCard.vue";
import i1 from "../assets/images/el1.png";
import i2 from "../assets/images/el2.png";
import i3 from "../assets/images/el3.png";

export default {
  data() {
    return {
      images: [
        {
          imagePath: i1,
          title: "Accessories",
          subtitle:
            "Complete your ensemble with designer accessories such as handbags, scarves, belts, and hats.",
        },
        {
          imagePath: i2,
          title: "Dresses",
          subtitle:
            "Explore a stunning range of designer dresses, including evening gowns and chic day dresses.",
        },
        {
          imagePath: i3,
          title: "Outerwear",
          subtitle:
            "Browse luxurious designer coats, jackets, and blazers to stay stylishly warm during colder seasons.",
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
    <h2>Designer Clothes For You</h2>
    <p>
      Immerse yourself in the world of luxury fashion with our meticulously
      crafted designer clothes!
    </p>
    <ul class="list">
      <ProductCard
        v-for="item in images"
        :key="item.imagePath"
        :imagePath="item.imagePath"
        :title="item.title"
        :subtitle="item.subtitle"
      />
    </ul>
  </Container>
</template>
<style scoped lang="scss">
@use "../assets/styles/functions" as *;
.container {
  padding-top: rem(281px);
  text-align: center;
}
h2 {
  font-family: "Roboto Slab";
  font-size: rem(50px);
  color: #224f34;
}
p {
  font-family: "Poppins";
  margin-top: rem(51px);
}
.list {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  margin-top: rem(72px);
  gap: rem(43px);
  & :deep(.title) {
    margin-bottom: rem(15px);
    font-size: rem(30px);
  }
}
</style>
