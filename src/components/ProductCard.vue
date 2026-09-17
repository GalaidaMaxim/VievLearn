<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    price: {
      type: String,
      required: true,
    },
    rating: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      required: true,
    },
    imagePath: {
      type: String,
      required: true,
    },
  },
};
</script>
<template>
  <li>
    <div :style="{ backgroundColor: color }" class="imageThumb">
      <img v-bind:src="imagePath" alt="" />
    </div>
    <p class="title">{{ title }}</p>
    <div class="price">
      <p>${{ price }}</p>
      <p>{{ rating }} <img src="../assets/images/fi-ss-star.png" alt="" /></p>
    </div>
  </li>
</template>
<style scoped>
.title {
  margin-top: 2.13rem;
  font-weight: 600;
  font-family: "Poppins";
}
.price {
  display: flex;
  justify-content: center;
  margin-left: auto;
  margin-right: auto;
  p {
    text-align: center;
    position: relative;
    font-family: "Poppins";
    padding-left: 1.7rem;
    &:last-child {
      padding-left: 2.1rem;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.3rem;
      &::before {
        content: "";
        border-left: 1px solid black;
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
      }
    }
    & img {
      display: inline-block;
      width: 1.1rem;
    }
  }
}
</style>
