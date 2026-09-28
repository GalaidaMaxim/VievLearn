<script>
import Container from "./Container.vue";
import FeedbackCard from "./FeedbackCard.vue";
export default {
  data() {
    return {
      active: 0,
    };
  },
  methods: {
    leftTurn() {
      this.active -= 1;
      if (this.active < 0) {
        this.active = 2;
      }
    },
    rightTurn() {
      this.active += 1;
      if (this.active > 2) {
        this.active = 0;
      }
    },
  },
  components: {
    Container,
    FeedbackCard,
  },
};
</script>

<template>
  <section>
    <Container class="container">
      <h2>Feedback Corner</h2>
      <ul>
        <FeedbackCard
          v-bind:class="{ active: active === 0 }"
          :title="'Emily Wilson'"
          :text="`The customer experience was exceptional from start to finish. The website is user-friendly, the checkout process was smooth, and the clothes I ordered fit perfectly. I'm beyond satisfied!`"
        />
        <FeedbackCard
          v-bind:class="{ active: active === 1 }"
          :title="'Sarah Thompson'"
          :text="`I absolutely love the quality and style of the clothing I purchased from this website. customer service was outstanding, and I received my order quickly. Highly recommended!`"
        />
        <FeedbackCard
          v-bind:class="{ active: active === 2 }"
          :title="'Olivia Martinez'"
          :text="`I had a great experience shopping on this website. The clothes I bought are fashionable and comfortable. Highly satisfied!`"
        />
      </ul>
      <div class="buttons">
        <button class="back" @click="leftTurn">
          <svg>
            <use href="../assets/images/Icons/sprite.svg#icon-arrow1" />
          </svg>
        </button>
        <button @click="rightTurn">
          <svg>
            <use href="../assets/images/Icons/sprite.svg#icon-arrow1" />
          </svg>
        </button>
      </div>
    </Container>
  </section>
</template>

<style scoped lang="scss">
@use "../assets/styles/functions" as *;

.container {
  padding-top: rem(247px);
  padding-bottom: rem(139px);
  text-align: center;
}
h2 {
  color: #224f34;
  font-family: "Roboto Slab";
  font-size: rem(50px);
}
ul {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: rem(37px);
  text-align: left;
  margin-top: rem(109px);
  & .active {
    background-color: #c2efd4;
    & :deep(.text) {
      color: #224f34;
    }
  }
}
.buttons {
  margin-top: rem(138px);
  .back {
    transform: rotateZ(180deg);
    margin-right: rem(51px);
  }
  button {
    background-color: transparent;
    border: none;
    width: rem(40px);
    height: rem(40px);
    border-radius: 4px;
    svg {
      width: rem(18px);
      height: 100%;
    }
    &:hover {
      background-color: #c2efd4;
      & svg {
        fill: #224f34;
      }
    }
  }
}
</style>
