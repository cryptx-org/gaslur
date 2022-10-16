<template>
  <div class="container">
    <div class="container__logo"><p>GASLUR</p></div>
    <div class="container__middle" ref="middleBtn" @click="addClass">
      <a class="btn">HOME</a>
      <a class="btn">MY PROFILE</a>
      <a class="btn">ACTIVITY</a>
      <a class="btn">HOW IT WORKS</a>
    </div>
    <div class="container__btn">
      <button class="create-btn">Create</button>
      <button class="sign-btn">Sign</button>
    </div>
    <div class="burger-icon" ref="brgBtn" @click="addClass">
      <div class="line1"></div>
      <div class="line2"></div>
      <div class="line3"></div>
    </div>
  </div>
</template>
<script>
export default {
  methods: {
    addClass() {
      this.$refs.brgBtn.classList.toggle("open");
      this.$refs.middleBtn.classList.toggle("open");
    },
  },
};
</script>
<style lang="scss" scoped>
.container {
  animation: ScrollY 0.5s ease-out;
  display: grid;
  padding: 5px;
  max-width: 100%;
  grid-template-columns: 1fr 2fr 1fr;
  color: $text-color;
  background-color: $bg-color;
  margin: 0 5rem;
  height: 5rem;
  font-family: "Poppins";
  font-style: normal;
  align-items: center;
}
.container__logo {
  display: flex;
  justify-content: flex-start;
  p {
    font-weight: 700;
    font-size: 32px;
    letter-spacing: 1.5px;
    background: linear-gradient(93.51deg, #9b51e0 2.84%, #3081ed 99.18%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
}
.container__middle {
  display: flex;
  justify-content: center;
  flex: 1 1 auto;
  min-width: 60%;

  transition: all 1s ease;
  .btn {
    margin: -1px 10px;
    cursor: pointer;
    font-weight: 500;
    font-size: 13px;
    margin-bottom: -1px;

    &:hover {
      background: linear-gradient(93.51deg, #9b51e0 2.84%, #3081ed 99.18%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      border-bottom: 1px solid #9b51e0;
    }
  }
}

.container__btn {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  font-size: 13px;
  font-weight: 500;
  letter-spacing: 1.5px;
  .create-btn {
    margin-right: 1rem;
    padding: 8px 25px;
    border-radius: 10px;
    border: 1px solid $text-color;
  }
  .create-btn:hover,
  .sign-btn:hover {
    background: linear-gradient(93.51deg, #9b51e0 2.84%, #3081ed 99.18%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .create-btn:hover {
    border: 1px solid #9b51e0;
  }
}
.burger-icon {
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-self: flex-end;
  align-self: center;
  display: none;
  cursor: pointer;
  margin-bottom: 6px;
}
.burger-icon > * {
  margin-top: 4px;
  border-radius: 20px;
  padding: 1px;
  width: 20px;
  background-color: white;
  transition: all 0.3s ease-in;
}

//media Queries
@media screen and (max-width: 900px) {
  //navBar
  .container__middle,
  .container__btn {
    display: none;
  }
  .container {
    margin: 0;
  }
  .container__logo {
    margin-left: 2rem;
  }
  .burger-icon {
    display: block;
    margin-right: 2rem;
  }
}
.open {
  z-index: 3;
  & .line1 {
    transform: rotate(45deg) translateY(8.5px);
  }
  & .line2 {
    transform: translateX(-10px);
    opacity: 0;
  }
  & .line3 {
    transform: rotate(-45deg) translateY(-8.5px);
  }
}
.container__middle.open {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding-top: 4rem;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background-color: rgba($color: #1f1d2b, $alpha: 0.9);
  backdrop-filter: blur(6px);

  & .btn {
    text-align: center;
    font-size: 1rem;
    margin-top: 2rem;
  }
}
</style>
