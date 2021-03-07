<template lang="pug">
  div.main-wrapper
    div.banners
      Hero
      AboutUs
      Initiatives
      Testimonial
</template>

<script>
import Hero from "@/components/home/Hero";
import AboutUs from "@/components/home/AboutUs";
import Initiatives from "@/components/home/Initiatives";
import Testimonial from "@/components/home/Testimonial";

export default {
  name: "Home",
  components: {
    Hero,
    AboutUs,
    Initiatives,
    Testimonial
  },
  data: () => ({
    drawer: true
  })
};
</script>
<style>
.main-wrapper {
  padding: 0;
}
.banners {
  overflow: hidden;
}
</style>