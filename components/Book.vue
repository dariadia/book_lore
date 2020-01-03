<template>
  <v-container>
    <v-card hover shaped>
      <v-card-title class="title_book"># books.one.episode_1.title</v-card-title>
      <v-row justify="space-between">
        <episode class="episode"></episode>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import Episode from "~/components/Episode.vue";

export default {
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

