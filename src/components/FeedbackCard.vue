<script>
export default {
  props: {
    title: {
      type: String,
    },
    text: String,
  },
};
</script>

<template>
  <li>
    <p class="qouters">“</p>
    <h3>{{ title }}</h3>
    <p class="text">{{ text }}</p>
  </li>
</template>

<style scoped lang="scss">
@use "../assets/styles/functions" as *;
li {
  padding-left: rem(19px);
  padding-right: rem(25px);
  padding-bottom: rem(29px);
  // outline: 2px solid red;
  border-radius: rem(5px);
  transition-duration: 500ms;
}
.qouters {
  font-family: "Noto Sans";
  font-size: rem(60px);
}
h3 {
  font-family: "Roboto Slab";
  color: #224f34;
}
.text {
  margin-top: rem(29px);
  font-size: rem(16px);
  font-family: "Poppins";
  line-height: rem(24px);
  color: #6e6e6e;
}
</style>
