<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <v-container style="height: 60px;"></v-container>
      <v-card>
        <v-card-title class="headline">The Series</v-card-title>
        <v-card-text>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione explicabo odit totam dicta consectetur accusamus, eius natus. Dicta, dolor quisquam porro deleniti quaerat quibusdam perspiciatis expedita nulla alias libero aperiam soluta modi voluptates veniam magni ab. Doloribus accusantium velit similique nemo magnam dolorum dicta repellat, cumque alias voluptatibus vel architecto?</p>
        </v-card-text>
        <book v-for="(book, i) in books" :key="i" :book="book" :book_index="i"></book>
        <v-container style="height: 30px;"></v-container>
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
        1: {
          1: {
            title: "At the Crossroads",
            src: "https://i.ibb.co/W5wzwHB/1.png",
            about: `One day your whole world crumbles around you. Literally. The sky splits, and everyone you know turns into dust. You escape to the thousands of glowing portals to any dimension imaginable. Only you are trapped in your world, and hundreds of other you-s don’t seem to care. That’s when a stranger appears and offers you a card, a key to any world. The price is high, and yet you take the chance. Your adventure begins at the Crossroads.`
          },
          2: {
            title: "Into the Abyss",
            src: "https://i.ibb.co/F8RTMkm/2.png",
            about: `You leave the Wands castle with the Mage. Consider it a field trip, you set out to travel across the universe and try everything you see. Cups, Swords, Pentacles – peoples with stitched mouths and half-felines. Also, apparently, the Black Emperor’s back (scary!), Maze is out there to get you, and the Sun guards her twin’s secrets. Your card is the key to any world, but can you wield it properly and will that be enough to survive?`
          },
          3: {
            title: "Against All Shadows",
            src: "https://i.ibb.co/FnLCq84/3.png",
            about: `in progress`
          }
        },
        2: {
          1: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg",
            about: `in progress`
          },
          2: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg",
            about: `in progress`
          },
          3: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg",
            about: `in progress`
          }
        },
        3: {
          1: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg",
            about: `in progress`
          },
          2: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg",
            about: `in progress`
          },
          3: {
            title: "in progress",
            src: "https://cdn.vuetifyjs.com/images/cards/store.jpg",
            about: `in progress`
          }
        }
      }
    };
  }
};
</script>