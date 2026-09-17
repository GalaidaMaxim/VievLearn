<script>
import Container from "./Container.vue";
export default {
  components: {
    Container,
  },
};
</script>

<template>
  <section>
    <Container class="herroContainer">
      <div class="left">
        <h1>Discover and Find Your Own Fashion!</h1>
        <p>
          Explore our curated collection of stylish clothing and accessories
          tailored to your unique taste.
        </p>
        <button>Explore now</button>
      </div>
      <div class="imageThumb">
        <img src="../assets/images/l1Small.png" alt="" />
      </div>
    </Container>
  </section>
</template>
<style scoped>
section {
  padding-top: 10.63rem;
  padding-bottom: 7.54rem;
  background-color: #c2efd4;
}
.herroContainer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
h1 {
  font-size: 3.9rem;
  color: #224f34;
  width: 29.5rem;
}
p {
  margin-top: 1.18rem;

  width: 25.68rem;
  font-family: "Poppins";
  font-style: normal;
  font-weight: 500;
  font-size: 1.1rem;
  line-height: 2rem;
  color: #267d49;
}

button {
  margin-top: 2.45rem;
  width: 11.72rem;
  height: 3.36rem;
  border-radius: 3px;
  background: #224f34;
  box-shadow: 6px 33px 59px rgba(0, 0, 0, 0.3);
  color: white;
  text-transform: uppercase;
  font-family: "Poppins";
  border: none;
}

.imageThumb {
  width: 25.9rem;
  height: 32, 59rem;
  min-height: 20px;
  background-color: rgba(107, 199, 133, 1);
  border-top-left-radius: 6.4rem;
  border-bottom-right-radius: 6.4rem;
  border-top-right-radius: 2.2rem;
  border-bottom-left-radius: 2.2rem;
}
</style>
