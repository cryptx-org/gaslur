<template lang="">
  <div class="heroContainer">
    <div class="heroContainer-1">
      <h1>Discover, collect, and charity in extraordinary NFT marketplace</h1>
      <p>
        In aenean posuere lorem risus nec. Tempor tincidunt aenean purus purus
        vestibulum nibh mi venenatis
      </p>
      <div class="btn-container">
        <button class="explore-btn">Explore</button>
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
  }
  .explore-btn {
    background: linear-gradient(
      103.91deg,
      #9b51e0 21.01%,
      rgba(48, 129, 237, 0.8) 100%
    );
    border-radius: 16px;
    padding: 0.5rem 4rem;
    margin-right: 2rem;
  }
}
</style>
