<template>
  <div class="container">
    <div class="container__logo"><p>GASLUR</p></div>
    <div class="container__middle">
      <a class="btn">HOME</a>
      <a class="btn">MY PROFILE</a>
      <a class="btn">ACTIVITY</a>
      <a class="btn">HOW IT WORKS</a>
    </div>
    <div class="container__btn">
      <button class="create-btn">Create</button>
      <button class="sign-btn">Sign</button>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.container {
  animation: ScrollY 0.5s ease-out;
  display: grid;

  width: 90%;
  grid-template-columns: 1fr 1fr 1fr;
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
  justify-content: space-around;
  .btn {
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
</style>
