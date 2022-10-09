<template lang="">
  <div class="auctionsContainer" id="Auctions">
    <div class="top-bar">
      <h1>HOT AUCTIONS</h1>
      <div class="view-btn">View all <v-icon>mdi-arrow-right</v-icon></div>
    </div>

    <Card />
  </div>
</template>
<script>
import Card from "./Card.vue";
export default {
  components: {
    Card,
  },
};
</script>
<style lang="scss" scoped>
.auctionsContainer {
  background-color: $bg-color;
  padding: 0 5rem;

  .top-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  h1 {
    color: #fff;
    font-weight: 500;
    font-size: 39px;
  }
  .view-btn {
    color: #d7d7d7;
    font-weight: 600;
    font-size: 20px;
    margin-right: 1.4rem;
    cursor: pointer;
  }
}
</style>
