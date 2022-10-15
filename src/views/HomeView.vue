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
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        console.log(entry);
        if (entry.isIntersecting && entry.target.id == "card") {
          entry.target.classList.add("animation");
        } else if (entry.isIntersecting && entry.target.id == "card1") {
          entry.target.classList.add("animation");
        } else if (entry.isIntersecting && entry.target.id == "icons") {
          entry.target.classList.add("scale");
        } else {
          entry.target.classList.remove("animation");
        }
      });
    });
    let target = document.getElementById("card");
    let target1 = document.getElementById("card1");
    let target2 = document.getElementById("icons");
    observer.observe(target);
    observer.observe(target1);
    observer.observe(target2);
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
.scale {
  animation: Scale 0.8s ease-in;
}
</style>
