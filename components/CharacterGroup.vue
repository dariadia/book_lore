<template>
  <div class="container">
    <h3 class="title_group character_book">{{group_name}}</h3>
    <v-card flat>
      <character v-for="(character, i) in characters" :key="i" :character="character" :card="i"></character>
    </v-card>
  </div>
</template>

<script>
import Character from "~/components/Character.vue";
export default {
  props: ["characters", "group_name"],
  components: {
    Character
  }
};
</script>