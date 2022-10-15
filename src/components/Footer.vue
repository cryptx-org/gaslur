<template lang="">
  <div class="footer">
    <p class="footer-text">
      Etiam et id tincidunt faucibus mollis a sociis pretium fermentum quis
      magna faucibus lacus.
    </p>
    <div class="marketplace">
      <strong>Marketplace</strong>
      <p>Home</p>
      <p>Activity</p>
      <p>Discover</p>
      <p>Learn more</p>
    </div>
    <div class="Company">
      <strong>Company</strong>
      <p>About Us</p>
      <p>Services</p>
      <p>Portfolio</p>
    </div>
    <div class="Contact">
      <strong>Contact</strong>
      <p>Facebook</p>
      <p>Twitter</p>
      <p>Instagram</p>
      <p>Email</p>
    </div>
  </div>
  <div class="socials">
    <div class="social-icons">
      <v-icon>mdi-facebook</v-icon>
      <v-icon>mdi-instagram</v-icon>
      <v-icon>mdi-twitter</v-icon>
    </div>
    <div class="copyrights">
      <p>Copyright 2022 Gaslur</p>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
.footer {
  background-color: $bg-color;
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr;
  color: #fff;
  padding: 0 5rem;

  .footer-text {
    max-width: 20rem;
    font-weight: 500;
    font-size: 30px;
  }
  .marketplace,
  .Company,
  .Contact {
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    strong {
      font-weight: 400;
      font-size: 33px;
    }
    p {
      font-weight: 400;
      font-size: 18px;
      color: #d7d7d7;
      cursor: pointer;
    }
  }
}
.socials {
  background-color: $bg-color;
  display: grid;
  grid-template-columns: 1fr 1fr;
  padding: 2rem 5rem;
  color: #e5e5e5;
  .copyrights {
    display: flex;
    justify-content: flex-end;
    margin-right: 8rem;
  }
  .copyrights,
  .social-icons {
    border-top: 1px solid #d7d7d7;
    padding-top: 1rem;
  }
  .social-icons > * {
    margin-right: 10px;
    cursor: pointer;
  }
}
</style>
