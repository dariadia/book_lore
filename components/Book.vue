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
}
</style>

