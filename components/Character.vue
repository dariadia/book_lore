<template>
  <v-avatar size="150">
    <img
      v-if="!character.img"
      src="https://www.appliedlogistics.co.nz/wp-content/uploads/2018/01/person-placeholder.jpg"
      alt="placeholder"
    />
    <!--placeholder till I crop the images-->

    <img v-else :src="character.img" :alt="character.name" />
  </v-avatar>
</template>

<script>
export default {
  props: ["character", "card"]
};
</script>