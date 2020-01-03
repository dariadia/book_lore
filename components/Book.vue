<template>
  <v-container>
    <v-card hover shaped>
      <v-card-title class="title_book">Book {{book_index}}</v-card-title>
      <v-row justify="space-between">
        <episode v-for="(episode, i) in book" :key="i" :episode="episode" class="episode"></episode>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import Episode from "~/components/Episode.vue";

export default {
  props: ["book", "book_index"],
  components: {
    Episode
  }
};
</script>

<style>
.episode {
  margin-left: 35px;
  margin-right: 35px;
}
.episode:hover {
  transition: 0.3s;
  -webkit-box-shadow: inset 7px 7px 91px -2px rgba(61, 245, 162, 0.42);
  -moz-box-shadow: inset 7px 7px 91px -2px rgba(61, 245, 162, 0.42);
  box-shadow: inset 7px 7px 91px -2px rgba(61, 245, 162, 0.42);
}
</style>

