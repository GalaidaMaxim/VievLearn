<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
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
    imageLeftGap: {
      type: String,
      default: "0px",
    },
    imageRightGap: {
      type: String,
      default: "0px",
    },
  },
  computed: {
    titleFontSize() {
      return this.subtitle ? "1.3rem" : "1rem";
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
    <p class="subtitle" v-if="subtitle">{{ subtitle }}</p>
    <div v-else class="price">
      <p>${{ price }}</p>
      <p>
        {{ rating }}
        <svg>
          <use href="../assets/images/Icons/sprite.svg#icon-star" />
        </svg>
      </p>
    </div>
  </li>
</template>
<style scoped lang="scss">
@use "../assets/styles/functions" as *;
.imageThumb {
  padding-left: v-bind(imageLeftGap);
  padding-right: v-bind(imageRightGap);
  overflow-y: hidden;
  background-color: v-bind(color);
}
.title {
  margin-top: 2.13rem;
  font-weight: 600;
  font-family: "Poppins";
  font-size: v-bind(titleFontSize);
}
.subtitle {
  font-family: "Poppins";
  text-align: center;
  padding-left: rem(15px);
  padding-right: rem(15px);
}
.price {
  display: flex;
  justify-content: center;
  margin-top: 0.36rem;
  p {
    text-align: right;
    position: relative;
    font-family: "Poppins";
    padding-right: 1.7rem;
    width: 50%;

    &:last-child {
      padding-left: 2.1rem;
      display: flex;
      align-items: center;
      justify-content: left;
      gap: rem(8px);
      width: 50%;

      &::before {
        content: "";
        border-left: 1px solid black;
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
      }
      & svg {
        display: block;
        width: rem(24px);
        height: rem(24px);
        fill: yellow;
      }
    }
    & img {
      display: inline-block;
      width: 1.1rem;
    }
  }
}
</style>
