<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <v-container style="height: 60px;"></v-container>
      <v-card>
        <v-card-title class="headline">The Series</v-card-title>
        <v-card-text>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione explicabo odit totam dicta consectetur accusamus, eius natus. Dicta, dolor quisquam porro deleniti quaerat quibusdam perspiciatis expedita nulla alias libero aperiam soluta modi voluptates veniam magni ab. Doloribus accusantium velit similique nemo magnam dolorum dicta repellat, cumque alias voluptatibus vel architecto?</p>
        </v-card-text>
        <book v-for="(book, i) in books" :key="i" v-model="books"></book>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import CardverseLogo from "~/components/CardverseLogo.vue";
import Book from "~/components/Book.vue";

export default {
  components: {
    CardverseLogo,
    Book
  },
  data() {
    return {
      books: {
        one: {
          episode_1: {
            title: "At the Crossroads",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg"
          },
          episode_2: {
            title: "Into the Abyss",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg"
          },
          episode_3: {
            title: "Against All Shadows",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg"
          }
        },
        two: {
          episode_1: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg"
          },
          episode_2: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg"
          },
          episode_3: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg"
          }
        },
        three: {
          episode_1: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg"
          },
          episode_2: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg"
          },
          episode_3: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg"
          }
        }
      }
    };
  }
};
</script>