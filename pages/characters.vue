<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <v-container style="height: 60px;"></v-container>
      <v-container>
        <v-card>
          <v-card-title class="headline">
            Characters
            <v-row class="d-flex justify-end">
              <v-btn-toggle tile v-model="opened_book">
                <v-btn
                  v-for="(book, i) in books"
                  :key="i"
                  class="ma-2"
                  tile
                  color="teal"
                  dark
                  @click="opened_book = (i + 1)"
                >Book {{book}}</v-btn>
              </v-btn-toggle>
            </v-row>
          </v-card-title>
          <v-card-text>
            <p>This is a spoiler-safe area, all characters are set to that of the begining of the picked book.</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione explicabo odit totam dicta consectetur accusamus, eius, tref. Lorem, ipsum dolor.</p>
          </v-card-text>
          <div v-if="opened_book == 0">
            <character-group
              v-for="(group, i) in book1_characters"
              :key="i"
              :characters="group"
              :group_name="i"
            ></character-group>
          </div>
          <div v-if="opened_book == 1">
            <character-group
              v-for="(group, i) in book2_characters"
              :key="i"
              :characters="group"
              :group_name="i"
            ></character-group>
          </div>
          <div v-if="opened_book == 2">
            <character-group
              v-for="(group, i) in book3_characters"
              :key="i"
              :characters="group"
              :group_name="i"
            ></character-group>
          </div>
          <v-container style="height: 30px;"></v-container>
        </v-card>
      </v-container>
    </v-flex>
  </v-layout>
</template>


<script>
import CharacterGroup from "~/components/CharacterGroup.vue";

export default {
  components: {
    CharacterGroup
  },
  data() {
    return {
      opened_book: 0,
      books: [1, 2, 3],
      book1_characters: {
        "major arcana": {
          Fool: { img: "" },
          Magician: {
            img: "https://i.ibb.co/VVPwt9M/magician.jpg",
            name: "Lars Jansen",
            power: "creation"
          },
          "High Priestess": {
            img:
              "https://cdn2.vectorstock.com/i/1000x1000/01/66/businesswoman-character-avatar-icon-vector-12800166.jpg"
          },
          Empress: {
            img: "",
            name: "Alisa Enisa Hajrovič"
          },
          Emperor: {
            img:
              "https://cdn.iconscout.com/icon/free/png-256/avatar-367-456319.png",
            name: "Gleb Kubitschek",
            power: "destruction"
          },
          Hierophant: {
            img:
              "https://cdn.iconscout.com/icon/free/png-256/avatar-372-456324.png"
          },
          Lovers: { img: "" },
          Chariot: { img: "https://i.ibb.co/VVPwt9M/magician.jpg" },
          Strength: { img: "" },
          Hermit: { img: "" },
          "Wheel of Fortune": { img: "" },
          Justice: { img: "" },
          "Hanged Man": { img: "" },
          Death: { img: "" },
          Temperance: { img: "" },
          Devil: { img: "" },
          Tower: { img: "", name: "Trixx" },
          Star: { img: "", name: "Deborah Rivlin" },
          Moon: { img: "", name: "Yana Lavrentyeva" },
          Sun: { img: "", name: "Anya Lavrentyeva" },
          Judgement: { img: "", name: "Maze Eaton Harper" },
          World: { img: "", name: "World", power: "portals" }
        },
        wands: {
          King: {
            img: "",
            name: "Theodore Jansen",
            power: "scepter: controls life energy of all the Wands"
          },
          Queen: { img: "", name: "Sara" }
        },
        swords: {
          King: {
            img: "",
            name: "Theodore Jansen",
            power: "sword: can slash through anything"
          }
        },
        pentacles: {},
        cups: {}
      },
      book2_characters: {
        "major arcana": {
          Fool: { img: "" },
          Magician: {
            img: "https://i.ibb.co/VVPwt9M/magician.jpg",
            name: "Lars Jansen",
            power: "creation"
          },
          "High Priestess": { img: "" },
          Empress: { img: "", name: "Alisa Enisa Hajrovič" },
          Emperor: { img: "", name: "Gleb Kubitschek", power: "destruction" },
          Hierophant: { img: "" },
          Lovers: { img: "" },
          Chariot: { img: "" },
          Strength: { img: "" },
          Hermit: { img: "", name: "Theodore Leven Jansen" },
          "Wheel of Fortune": { img: "" },
          Justice: { img: "" },
          "Hanged Man": { img: "" },
          Death: { img: "" },
          Temperance: { img: "" },
          Devil: { img: "" },
          Tower: { img: "", name: "Trixx" },
          Star: { img: "", name: "Deborah Rivlin" },
          Moon: { img: "", name: "Yana Lavrentyeva" },
          Sun: { img: "", name: "Anya Lavrentyeva" },
          Judgement: { img: "", name: "World" },
          World: { img: "", name: "World", power: "portals" }
        },
        wands: {},
        swords: {},
        pentacles: {},
        cups: {}
      },
      book3_characters: {
        "major arcana": {
          Fool: { img: "", name: "Cassandra Murphy" },
          Magician: {
            img: "https://i.ibb.co/VVPwt9M/magician.jpg",
            name: "Lars Jansen",
            power: "creation"
          },
          "High Priestess": { img: "" },
          Empress: { img: "" },
          Emperor: { img: "" },
          Hierophant: { img: "" },
          Lovers: { img: "" },
          Chariot: { img: "" },
          Strength: { img: "" },
          Hermit: { img: "" },
          "Wheel of Fortune": { img: "" },
          Justice: { img: "" },
          "Hanged Man": { img: "" },
          Death: { img: "" },
          Temperance: { img: "" },
          Devil: { img: "" },
          Tower: { img: "" },
          Star: { img: "" },
          Moon: { img: "" },
          Sun: { img: "" },
          Judgement: { img: "" },
          World: { img: "", name: "World", power: "portals" }
        },
        wands: {},
        swords: {},
        pentacles: {},
        cups: {}
      }
    };
  }
};
</script>