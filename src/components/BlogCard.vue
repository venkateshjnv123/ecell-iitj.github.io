<template>
  <v-layout row wrap>
    <v-card
      :elevation="10"
      md3
      style="border-radius:30px"
      class="mx-auto cardstyle"
    >
      <v-img
        :src="blog.thumbnail"
        height="200px"
        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
        style="margin-bottom:10px;"
      >
      </v-img>
      <v-card-title
        v-text="blog.title"
        style="overflow-y: auto;height:170px"
      ></v-card-title>
      <v-card-subtitle
        style="margin-top:10px; font-size:17px;"
        v-text="blog.author"
      >
      </v-card-subtitle>
      <v-card-actions class="mar2">
        <v-btn
          dark
          color="#2D71C9"
          rounded
          style="margin-top:0px; margin-left: 33%"
          small
          v-if="blog.link != null"
          :href="blog.link"
        >
          <a class="white--text text-decoration-none"></a>
          Read More
        </v-btn>
      </v-card-actions>
      <v-expansion-panels flat>
        <v-expansion-panel>
          <v-expansion-panel-header class="details">
            Tags
            <template v-slot:actions>
              <v-icon color="pink">$expand</v-icon>
            </template>
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <div style="height:120px">
              <v-chip
                v-for="tags in blog.categories"
                :key="tags.name"
                class="ma-2"
                small
                color="deep-purple accent-4"
                outlined
                >{{ tags }}
              </v-chip>
            </div>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-card>
  </v-layout>
</template>
<script>
export default {
  name: "BlogC",
  props: ["blog"]
};
</script>

<style>
/* global scope for override v-btn styles */
button.v-btn,
button.v-expansion-panel-header {
  outline: none;
}
</style>

<style scoped>
.header {
  color: white;
  text-align: center;
  font-weight: 400;
}
.cardstyle {
  margin-top: 60px;
  width: 320px;
  background-image: linear-gradient(
    45deg,
    #edeaeb 25%,
    #ffffff 25%,
    #ffffff 50%,
    #edeaeb 50%,
    #edeaeb 75%,
    #ffffff 75%,
    #ffffff 100%
  );
}
.mar {
  margin-left: 20px;
  margin-right: 20px;
}
.details {
  font-weight: 500;
  outline: none;
}
.mar2 {
  margin-bottom: 20px;
  margin-top: 20px;
}
</style>
