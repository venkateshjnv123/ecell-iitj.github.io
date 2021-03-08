<template>
  <v-img dark src="../../assets/Initiatives.jpg" style="height: auto;">
    <v-container class="pa-4 text-center">
      <v-row class="fill-height" align="center" justify="center">
        <h3
          class="display-3 font-weight-bold mb-10"
          style="color:rgb(255,255,255)"
        >
          Our Initiatives
        </h3>
        <h4 class="mb-5" style="color:rgb(255,255,255)">
          "We at E-Cell, IIT Jodhpur believe that entrepreneurship is the key to
          India’s development. To fulfill this vision, we have conceptualized &
          successfully implemented various initiatives to help students, young
          entrepreneurs & professionals in their entrepreneurial journey."
        </h4>
        <template v-for="(item, i) in items">
          <v-col :key="i" cols="12" md="4">
            <v-hover v-slot="{ hover }">
              <v-card
                :elevation="hover ? 12 : 2"
                :class="{ 'on-hover': hover }"
              >
                <v-img :src="item.img" height="225px">
                  <v-card-title class="title white--text">
                    <v-row
                      class="fill-height flex-column"
                      justify="space-between"
                    >
                      <p class="mt-4 subheading text-center">
                        {{ item.title }}
                      </p>

                      <div>
                        <p
                          class="ma-0 body-1 font-weight-bold font-italic text-center"
                        >
                          {{ item.text }}
                        </p>
                        <p
                          class="caption font-weight-medium font-italic text-center"
                        >
                          {{ item.subtext }}
                        </p>
                      </div>
                    </v-row>
                  </v-card-title>
                </v-img>
              </v-card>
            </v-hover>
          </v-col>
        </template>
      </v-row>
    </v-container>
  </v-img>
</template>

<script>
export default {
  data: () => ({
    icons: ["mdi-rewind", "mdi-play", "mdi-fast-forward"],
    items: [
      {
        title: "New Releases",
        text: `It's New Release Friday`,
        subtext: "Newly released songs. Updated daily.",
        img: "http://lorempixel.com/output/nightlife-q-c-640-480-5.jpg"
      },
      {
        title: "Rock",
        text: "Greatest Rock Hits",
        subtext: "Lose yourself in rock tunes.",
        img:
          "https://images.unsplash.com/photo-1498038432885-c6f3f1b912ee?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2100&q=80"
      },
      {
        title: "Mellow Moods",
        text: "Ambient Bass",
        subtext: "Chill beats to mellow you out.",
        img: "http://lorempixel.com/output/abstract-q-c-640-480-6.jpg"
      },
      {
        title: "New Releases",
        text: `It's New Release Friday`,
        subtext: "Newly released songs. Updated daily.",
        img: "http://lorempixel.com/output/nightlife-q-c-640-480-5.jpg"
      },
      {
        title: "Rock",
        text: "Greatest Rock Hits",
        subtext: "Lose yourself in rock tunes.",
        img:
          "https://images.unsplash.com/photo-1498038432885-c6f3f1b912ee?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2100&q=80"
      },
      {
        title: "Mellow Moods",
        text: "Ambient Bass",
        subtext: "Chill beats to mellow you out.",
        img: "http://lorempixel.com/output/abstract-q-c-640-480-6.jpg"
      }
    ],
    transparent: "rgba(255, 255, 255, 0)"
  })
};
</script>
<style scoped>
.v-card {
  transition: opacity 0.4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.6;
}

.Background {
  &:before {
    content: "";
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: rgb(0, 0, 0);
    opacity: 0.6;
  }
}
</style>
