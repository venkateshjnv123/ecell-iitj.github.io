<template>
  <v-parallax
    dark
    src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
    style="height: 95vh;"
  >
    <v-row align="center" justify="center">
      <v-col class="text-center" cols="12">
        <v-img
          max-height="200"
          max-width="300"
          class="mb-10 mx-auto"
          src="@/assets/ecell_logo.png"
        ></v-img>
        <h1
          :class="[
            $vuetify.breakpoint.lgAndUp
              ? 'display-3 font-weight-bold mb-10'
              : 'h3 font-weight-bold mb-10'
          ]"
        >
          THE ENTREPRENEURSHIP CELL IIT Jodhpur
        </h1>
        <h4 :class="[$vuetify.breakpoint.lgAndUp ? 'display-1' : 'display-1']">
          "IGNITE | INNOVATE | INSPIRE"
        </h4>
      </v-col>
    </v-row>
  </v-parallax>
</template>
