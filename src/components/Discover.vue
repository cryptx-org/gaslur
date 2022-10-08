<template lang="">
  <div class="discover">
    <div class="discoverNav">
      <div class="discoverlogo">
        <p>DISCOVER</p>
      </div>
      <div class="discoverbuttons">
        <p><v-icon>mdi-sort-variant</v-icon>Category</p>
        <p>Cheapest<v-icon>mdi-chevron-down</v-icon></p>
        <p>Newest<v-icon>mdi-chevron-down</v-icon></p>
        <button><v-icon>mdi-filter</v-icon>Filter</button>
      </div>
    </div>
    <div class="discovercards">
      <DiscoverCards />
    </div>
    <div class="loadbutton">
      <button>LOAD MORE</button>
    </div>
  </div>
</template>
<script>
import DiscoverCards from "./DiscoverCards.vue";
export default {
  components: {
    DiscoverCards,
  },
};
</script>
<style lang="scss">
.discover {
  background-color: $bg-color;
  width: 100vw;
  padding: 0 5rem;
  color: white;
}
.discoverNav {
  display: grid;
  grid-template-columns: 2fr 1fr;
  align-items: center;

  padding-bottom: 2rem;
  .discoverlogo {
    font-weight: 500;
    font-size: 38px;
  }
  .discoverbuttons {
    font-weight: 500;
    font-size: 16px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    gap: 3px;
    margin-right: 1.5rem;
    p {
      cursor: pointer;
    }
    button {
      background: linear-gradient(93.51deg, #9b51e0 2.84%, #3081ed 99.18%);
      border-radius: 10px;
      padding: 5px;
    }
  }
}
.loadbutton {
  padding: 5rem;
  text-align: center;
  button {
    border: 1px solid #bcbcbc;
    border-radius: 10px;
    padding: 5px 20px;
    font-weight: 500;
    font-size: 12px;
  }
}
</style>
