<template lang="">
  <div class="heroContainer">
    <div class="heroContainer-1">
      <h1>Discover, collect, and charity in extraordinary NFT marketplace</h1>
      <p>
        In aenean posuere lorem risus nec. Tempor tincidunt aenean purus purus
        vestibulum nibh mi venenatis
      </p>
      <div class="btn-container">
        <a class="explore-btn" href="#Auctions">Explore</a>
        <button class="create-btn">Create</button>
      </div>
    </div>
    <div class="heroContainer-2">
      <v-img src="@/assets/Herocard.png" class="herocard"></v-img>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
.heroContainer {
  display: grid;
  grid-template-columns: 1fr 1fr;
  background-color: $bg-color;
  padding: 5rem;
}
.heroContainer-1 {
  animation: ScrollX 0.5s ease-out;
  display: flex;
  justify-content: center;
  flex-direction: column;
  h1 {
    font-weight: 600;
    font-size: 72px;
    color: white;
    letter-spacing: 1px;
    line-height: 82px;
  }
  p {
    font-weight: 400;
    font-size: 24px;
    letter-spacing: 0.5px;
    color: #e2e2e2;
  }
}
.heroContainer-2 {
  animation: Scale 0.5s ease-in;
  display: flex;
  align-items: center;
  .herocard {
    height: 34rem;
  }
}
.btn-container {
  margin-top: 1rem;
  color: #d7d7d7;
  font-weight: 600;
  font-size: 24px;
  .create-btn {
    padding: 0.5rem 4rem;
    border-radius: 16px;
    border: 1px solid $text-color;
    &:hover {
      background: linear-gradient(93.51deg, #9b51e0 2.84%, #3081ed 99.18%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      border-color: #9b51e0;
      animation: ButtonScale 0.5s ease-out;
    }
  }
  .explore-btn {
    text-decoration: none;
    color: white;
    background: linear-gradient(
      103.91deg,
      #9b51e0 21.01%,
      rgba(48, 129, 237, 0.8) 100%
    );
    border-radius: 16px;
    padding: 0.5rem 4rem;
    margin-right: 2rem;
    &:hover {
      animation: ButtonScale 0.5s ease-out;
    }
  }
}

//meadia queries
@media screen and (max-width: 900px) {
  .heroContainer {
    grid-template-columns: 1fr;
    padding: 4rem 1rem;
  }
  .heroContainer-2 {
    display: none;
  }
  .heroContainer-1 {
    justify-self: center;
    text-align: center;
    max-width: 80%;
    h1 {
      font-size: 2.5em;
      line-height: 50px;
    }
    p {
      font-size: 1.2em;
      margin-bottom: 3rem;
    }
  }
  .btn-container {
    display: flex;
    flex-wrap: wrap;
    margin: 0.5rem auto;
    max-width: 14rem;
    .explore-btn {
    }
    .create-btn {
      margin-top: 2rem;
    }
  }
}
</style>
