<script>
import i8 from "../assets/images/ingreen.png";

import Container from "./Container.vue";
import DotsBlock from "./DotsBlock.vue";

export default {
  data() {
    return {
      i8,
      time: 20.01 * 3600,
      clicerID: null,
    };
  },
  methods: {
    timeMinus() {
      this.time -= 1;
    },
    getHour() {
      return Math.floor(this.time / 3600);
    },
    getMinutes() {
      return Math.floor((this.time - this.getHour() * 3600) / 60);
    },
    getSecconds() {
      return this.time - this.getHour() * 3600 - this.getMinutes() * 60;
    },
    transformTimer(time) {
      return time > 9 ? time : `0${time}`;
    },
  },
  mounted() {
    this.clicerID = setInterval(this.timeMinus, 1000);
  },
  unmounted() {
    clearInterval(this.clicerID);
  },
  components: {
    Container,
    DotsBlock,
  },
};
</script>

<template>
  <section>
    <Container class="container">
      <div class="imageContainer">
        <DotsBlock class="dots" :width="4" :height="4" />
        <img v-bind:src="i8" alt="123" />
      </div>
      <div>
        <h2>Exclusive offer</h2>
        <p class="subtitle">
          Unlock the ultimate style upgrade with our exclusive offer Enjoy
          savings of up to 40% off on our latest New Arrivals
        </p>
        <div class="clock">
          <div>
            <p class="time">{{ this.transformTimer(this.getHour()) }}</p>
            <p class="n">Days</p>
          </div>
          <div>
            <p class="time">{{ this.transformTimer(this.getMinutes()) }}</p>
            <p class="n">Hours</p>
          </div>
          <div>
            <p class="time">{{ this.transformTimer(this.getSecconds()) }}</p>
            <p class="n">Min</p>
          </div>
        </div>
        <button>buy Now</button>
      </div>
    </Container>
  </section>
</template>

<style scoped lang="scss">
@use "../assets/styles/functions" as *;
.container {
  background-color: #c2efd4;
  padding-left: rem(81px);
  display: flex;
  align-items: center;
  gap: rem(104px);
}
.dots {
  position: absolute;
  left: rem(-32px);
  bottom: rem(41px);
}
.imageContainer {
  width: rem(482px);
  position: relative;
}
h2 {
  font-family: "Roboto Slab";
  color: #224f34;
  font-size: rem(46px);
}
.subtitle {
  color: #224f34;
  width: rem(589px);
  font-family: "Poppins";
  line-height: rem(24px);
  margin-top: rem(20px);
}
.clock {
  display: flex;
  margin-top: rem(77px);
  gap: rem(35px);
  & div {
    background-color: white;
    width: rem(100px);
    height: rem(100px);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    & .time {
      font-family: "Poppins";
      color: #224f34;
      font-weight: 600;
      line-height: rem(48px);
      font-size: rem(32px);
    }
    & .n {
      font-family: "Poppins";
      color: #224f34;
      font-size: rem(16px);
    }
  }
}

button {
  background-color: #224f34;
  width: rem(235px);
  height: rem(74px);
  text-transform: uppercase;
  font-family: "Poppins";
  color: white;
  font-weight: 600;
  font-size: rem(20px);
  border: none;
  margin-top: rem(41px);
}
</style>
