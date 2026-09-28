<script>
export default {
  data() {
    return {
      arr: [],
    };
  },
  props: {
    width: { default: 3 },
    height: { default: 3 },
  },
  mounted() {
    for (let i = 0; i < this.width * this.height; i++) {
      this.arr.push(i);
    }
  },
};
</script>
<template>
  <div class="cover">
    <svg v-for="item in this.arr" :key="item" class="dot">
      <use href="../assets/images/Icons/sprite.svg#icon-elipce" />
    </svg>
  </div>
</template>
<style scoped lang="scss">
@use "../assets/styles/functions" as *;
.cover {
  display: grid;
  grid-template-columns: repeat(v-bind(width), rem(8px));
  gap: rem(29px);
}
.dot {
  width: rem(8px);
  height: rem(8px);
  fill: #267144;
}
</style>
