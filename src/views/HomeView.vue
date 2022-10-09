<template lang="">
  <div class="body">
    <Navbar />
    <Hero />
    <Auctions />
    <Startingsec />
    <Discover />
    <Footer />
  </div>
</template>
<script>
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import Auctions from "@/components/Auctions.vue";
import Startingsec from "@/components/Startingsec.vue";
import Discover from "@/components/Discover.vue";
import Footer from "@/components/Footer.vue";
export default {
  mounted() {
    const observer = new IntersectionObserver((entries, observer) => {
      entries.forEach((entry) => {
        console.log("Observed");
        entry.target.classList.add("animation");
        observer.unobserve(entry.target);
      });
    });
    observer.observe(document.getElementById("test"));
  },
  components: {
    Navbar,
    Hero,
    Auctions,
    Startingsec,
    Discover,
    Footer,
  },
};
</script>
<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: "Poppins";
  font-style: normal;
  scroll-behavior: smooth;
}
.body {
  height: 100vh;
  background: $bg-color;
}
.animation {
  animation: ScrollX 1s ease-in;
}
</style>
