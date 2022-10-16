<template lang="">
  <div class="card-container">
    <v-row id="card">
      <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
        <v-card min-width="13rem" flat color="#1f1d2b">
          <v-img :src="card.src" height="313px"> </v-img>

          <div class="cardtext-container">
            <div class="text-1" v-text="card.title"></div>
            <div class="text-2" v-text="card.price"></div>
          </div>
          <div class="info-container">
            <p>
              Ends in
              <strong style="color: #fff; font-size: 12px; font-weight: 400">
                {{ card.end }}
              </strong>
            </p>
            <button class="bid-btn">Bid</button>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  data: () => ({
    cards: [
      {
        title: "Lorem Ipsum",
        price: "1.20 Weth",
        src: require("@/assets/nft_pic1.png"),
        end: "01.34.35",
        flex: 3,
      },
      {
        title: "Dolor sit amet",
        price: "0.21 Weth",
        src: require("@/assets/nft_pic2.png"),
        end: "01.34.35",
        flex: 3,
      },
      {
        title: "Dignism curabitu..",
        price: "0.01 Weth",
        src: require("@/assets/nft_pic3.png"),
        end: "01.34.35",
        flex: 3,
      },
      {
        title: "Amet pellentesq..",
        price: "0.55 Weth",
        src: require("@/assets/nft_pic4.png"),
        end: "01.34.35",
        flex: 3,
      },
    ],
  }),
};
</script>
<style lang="scss" scoped>
.card-container {
  width: 100%;
}
.cardtext-container {
  display: flex;
  justify-content: space-between;
  font-weight: 600;
  font-size: 14px;
  padding: 1rem 0;
  color: #fff;
  border-bottom: 1px solid #fff;
}
.info-container {
  display: flex;
  justify-content: space-between;
  padding: 1rem 0;
  color: #fff;
  font-weight: 400;
  font-size: 13px;
  color: #bcbcbc;
  .bid-btn {
    padding: 2px 23px;
    border: 1px solid white;
    border-radius: 8px;
  }
}

//media queries
@media screen and (max-width: 900px) {
  .v-col-3 {
    max-width: 70%;
  }
  .v-row {
    display: flex;
    justify-content: center;
  }
}
</style>
