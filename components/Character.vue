<template>
  <v-hover v-slot:default="{ hover }">
    <v-card class="d-inline-block mx-auto" flat>
      <v-card-text class="panel_character-img">
        <v-avatar size="150">
          <!--placeholder till I crop the images-->
          <img
            v-if="!character.img"
            src="https://www.appliedlogistics.co.nz/wp-content/uploads/2018/01/person-placeholder.jpg"
            alt="placeholder"
          />
          <img v-else :src="character.img" :alt="character.name" />
          <v-expand-transition>
            <div
              v-if="hover && character.name"
              class="d-flex transition-fast-in-fast-out black darken-3 v-card--reveal display-1 white--text"
              style="height: 60%;"
            >{{character.name}}</div>
          </v-expand-transition>
        </v-avatar>
      </v-card-text>
      <v-card-title class="title_character-card justify-center">The {{card}}</v-card-title>
    </v-card>
  </v-hover>
</template>

<script>
export default {
  props: ["character", "card"]
};
</script>

<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}
</style>