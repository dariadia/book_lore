<template>
  <v-col justify="space-between">
    <v-img height="300" width="200" v-bind:src="episode.src"></v-img>
    <h3 class="title_episode">Episode {{episode.title}}</h3>
  </v-col>
</template>


<script>
export default {
  props: ["episode"]
};
</script>