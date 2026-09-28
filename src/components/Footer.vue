<script>
import Container from "./Container.vue";
export default {
  components: {
    Container,
  },
};
</script>
<template>
  <Container class="container">
    <div class="top">
      <p class="logo">Rivo</p>
      <p class="title">SHOP</p>
      <p class="title">Company</p>
      <p class="title">Stay up to date</p>
      <div class="social">
        <p class="title">Social Media</p>
        <div class="links">
          <button>
            <svg>
              <use href="../assets/images/Icons/sprite.svg#icon-facebook" />
            </svg>
          </button>
          <button>
            <svg>
              <use href="../assets/images/Icons/sprite.svg#icon-twitter" />
            </svg>
          </button>
          <button>
            <svg>
              <use href="../assets/images/Icons/sprite.svg#icon-instagram" />
            </svg>
          </button>
        </div>
      </div>
      <ul class="links">
        <li class="text">Products</li>
        <li class="text">Overview</li>
        <li class="text">Pricing</li>
        <li class="text">Releases</li>
      </ul>
      <ul class="links">
        <li class="text">About us</li>
        <li class="text">Contact</li>
        <li class="text">News</li>
        <li class="text">Support</li>
      </ul>
      <form>
        <input type="text" placeholder="Enter your email" />
        <button>SUBMIT</button>
      </form>
    </div>
    <div class="bottom">
      <div class="line"></div>
      <p>Terms</p>
      <p>Privacy</p>
      <p>Cookies</p>
    </div>
  </Container>
</template>

<style scoped lang="scss">
@use "../assets/styles/functions" as *;
.container {
  padding-top: rem(80px);
  padding-bottom: rem(82px);
}
p,
li {
  color: white;
}
.logo {
  font-family: sans-serif;
  font-weight: 500;
  font-size: rem(50px);
  line-height: 1;
}
.top {
  display: grid;
  grid-template-columns: rem(398px) rem(207px) rem(257px) auto;
}
.title {
  font-family: "Roboto Slab";
  font-weight: 500;
  text-transform: uppercase;
  margin-top: auto;
}
.social {
  padding-top: rem(44px);
  & .title {
    text-transform: none;
  }
  .links {
    display: flex;
    gap: rem(36px);
  }
  button {
    padding: 0;
    width: rem(35px);
    height: rem(35px);
    background-color: transparent;
    border: none;
    flex-shrink: 0;
    transform: none;
    transition-duration: 500ms;
    transition-property: transform;
    &:hover {
      transform: scale(1.5);
    }
    & svg {
      width: 100%;
      height: 100%;
      display: block;
      fill: white;
    }
  }
}
.links {
  padding-top: rem(25px);
  .text {
    font-family: "Poppins";
    font-size: rem(20px);
    &:not(:first-child) {
      margin-top: rem(18px);
    }
  }
}
form {
  padding-top: rem(52px);
  display: flex;
  & input {
    width: rem(327px);
    height: rem(57px);
    padding-left: rem(28px);
    background-color: transparent;
    border: 2px solid #a3f3be;
    font-family: "Poppins";
    font-size: rem(20px);
    color: white;
    &:active,
    &:focus {
      outline: none;
    }
    &::placeholder {
      font-family: "Poppins";
      font-size: rem(20px);
      color: white;
    }
  }
  & button {
    width: rem(115px);
    height: rem(57px);
    border-radius: 0;
    border: none;
    background-color: #a3f3be;
    font-family: "Poppins";
    font-size: rem(20px);
  }
}
.bottom {
  margin-top: rem(154px);
  display: flex;
  gap: rem(35px);
  align-items: center;
  .line {
    border-top: 2px solid white;
    flex-grow: 1;
  }
  p {
    font-family: "Poppins";
    font-weight: 600;
    font-size: rem(20px);
  }
}
</style>
