<template>
  <v-expansion-panels focusable multiple>
    <v-expansion-panel class="panel_episode">
      <v-expansion-panel-header>
        <v-col justify="space-between">
          <v-img height="300" width="200" :src="episode.src" :alt="episode.title" />
          <h3 class="title_episode">Episode {{episode_index}}</h3>
          <h3 class="title_episode">{{episode.title}}</h3>
        </v-col>
      </v-expansion-panel-header>
      <v-expansion-panel-content>{{episode.about}}</v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>
</template>


<script>
export default {
  props: ["episode", "episode_index"]
};
</script>