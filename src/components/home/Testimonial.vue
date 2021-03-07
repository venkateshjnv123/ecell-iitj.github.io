<template>
  <v-parallax dark src="../../assets/testi1.jpg" style="height: 100%; ">
    <v-carousel
      cycle
      height="650"
      hide-delimiter-background
      show-arrows-on-hover
    >
      <v-carousel-item v-for="(item, i) in items" :key="i">
        <v-row
          class="fill-height flex-column pa-4"
          align="center"
          justify="center"
        >
          <div align="center" justify="center">
            <v-img
              :src="item.src"
              style="border-radius: 20px"
              height="200px"
              width="200px"
            ></v-img>
            <p class="mt-10 subheading text-center">
              {{ item.text }}
            </p>
            <p class="ma-0 body-1 font-weight-bold font-italic text-center">
              {{ item.name }}
            </p>
            <p class="caption font-weight-medium font-italic text-center">
              {{ item.company }}
            </p>
          </div>
        </v-row>
      </v-carousel-item>
    </v-carousel>
  </v-parallax>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
          text:
            "YOU GUYS HAVE PUT UP A MASSIVE PLATFORM WHICH WILL BE THE ONE THAT BUILDS THE UNICORNS OF TOMORROW.",
          name: "TRAVIS KALANICK",
          company: "EX-CEO, UBER"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
          text:
            "YOU GUYS HAVE PUT UP A MASSIVE PLATFORM WHICH WILL BE THE ONE THAT BUILDS THE UNICORNS OF TOMORROW.",
          name: "TRAVIS KALANICK",
          company: "EX-CEO, UBER"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
          text:
            "YOU GUYS HAVE PUT UP A MASSIVE PLATFORM WHICH WILL BE THE ONE THAT BUILDS THE UNICORNS OF TOMORROW.",
          name: "TRAVIS KALANICK",
          company: "EX-CEO, UBER"
        },
        {
          src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg",
          text:
            "YOU GUYS HAVE PUT UP A MASSIVE PLATFORM WHICH WILL BE THE ONE THAT BUILDS THE UNICORNS OF TOMORROW.",
          name: "TRAVIS KALANICK",
          company: "EX-CEO, UBER"
        }
      ]
    };
  }
};
</script>
