<template lang="">
  <div class="iconCard">
    <div class="blur"></div>
    <v-row id="icons">
      <v-col
        v-for="iconcard in IconCards"
        :key="iconcard.text"
        :cols="iconcard.flex"
      >
        <div class="iconcard-container">
          <div class="icon-container">
            <v-icon size="3rem">{{ iconcard.icon }}</v-icon>
          </div>
          <p>{{ iconcard.text }}</p>
        </div>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  data: () => ({
    IconCards: [
      {
        icon: "mdi-shield-check-outline",
        text: "Connect your wallet",
        flex: 3,
      },
      {
        icon: "mdi-storefront-outline",
        text: "Posuere urna, sit amet molestie leo",
        flex: 3,
      },
      {
        icon: "mdi-image",
        text: "Semper pretium libero sed quam ac integer ut",
        flex: 3,
      },
      {
        icon: "mdi-rocket-launch",
        text: "Lectus volutpat magna vitae in arcu",
        flex: 3,
      },
    ],
  }),
};
</script>
<style lang="scss" scoped>
.iconCard {
  margin: 6rem 9rem;
}
.icon-container {
  width: 9rem;
  height: 8rem;
  background: rgba(255, 255, 255, 0.095);
  box-shadow: inset 2.01px -2.01px 20px rgba(214, 214, 214, 0.17),
    inset -3.01333px 3.01333px 3.01333px rgba(255, 255, 255, 0.39);
  backdrop-filter: blur(37.2147px);
  border-radius: 26px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.iconcard-container {
  display: flex;
  flex-direction: column;
  align-items: center;

  p {
    text-align: center;
    max-width: 8rem;
    font-weight: 400;
    font-size: 12px;
    margin-top: 1rem;
  }
}
.blur {
  background: linear-gradient(93.51deg, #9b51e0 2.84%, #3081ed 99.18%);
  filter: blur(100px);
  border-radius: 10px;
  width: 80vw;
  height: 10rem;
  position: absolute;
  opacity: 0.5;
}
@media screen and (max-width: 900px) {
  .v-col-3 {
  }
  .v-row {
    justify-content: center;
  }
  .iconCard {
    padding: 3rem 0;
    margin: 0;
    min-width: 20%;
  }
}
</style>
