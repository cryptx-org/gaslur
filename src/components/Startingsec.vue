<template lang="">
  <div class="start-container">
    <div class="text-container">
      <h1>Getting Started</h1>
      <p>Eu, molestie commodo, enim pellentesque turpis integer sagittis</p>
    </div>
    <IconCard />
  </div>
</template>
<script>
import IconCard from "./IconCard.vue";
export default {
  components: {
    IconCard,
  },
};
</script>
<style lang="scss" scoped>
.start-container {
  width: 100%;
  padding-bottom: 5rem;
  background-color: $bg-color;
  display: flex;
  padding-top: 5rem;
  flex-direction: column;
  color: white;
}
.text-container {
  text-align: center;
  h1 {
    font-weight: 500;
    font-size: 40px;
  }
  p {
    font-weight: 400;
    font-size: 18px;
    color: #e2e2e2;
  }
}

//media queries
@media screen and (max-width: 900px) {
  .text-container {
    margin: 1rem;
    h1 {
      font-size: 2em;
    }
  }
}
</style>
