<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <v-container style="height: 60px;"></v-container>
      <div class="text-center">
        <cardverse-logo />
        <logo />
        <vuetify-logo />
      </div>
      <v-card>
        <v-card-title class="headline">Welcome to the Lore Guide</v-card-title>
        <v-card-text>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque nulla, laudantium aut corporis praesentium possimus. Atque porro laborum harum esse, nisi voluptates itaque vitae quis deleniti explicabo quam unde quas placeat eligendi nihil et animi nemo nulla ducimus? Dignissimos unde explicabo nobis eum quia voluptate dolorem vitae at culpa. Earum.</p>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque nulla, laudantium aut corporis praesentium possimus. Atque porro laborum harum esse, nisi voluptates itaque vitae quis deleniti explicabo quam unde quas placeat eligendi nihil et animi nemo nulla ducimus? Dignissimos unde explicabo nobis eum quia voluptate dolorem vitae at culpa. Earum.</p>
          <div class="d-flex justify-center">
            <v-img
              max-width="400px"
              class="mb-6"
              src="https://cdn.shopify.com/s/files/1/0027/9642/1155/products/Adventure_Awaits-black_with_colour_2000x.png?v=1555941230"
            />
          </div>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque nulla, laudantium aut corporis praesentium possimus. Atque porro laborum harum esse, nisi voluptates itaque vitae quis deleniti explicabo quam unde quas placeat eligendi nihil et animi nemo nulla ducimus? Dignissimos unde explicabo nobis eum quia voluptate dolorem vitae at culpa. Earum.</p>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque nulla, laudantium aut corporis praesentium possimus. Atque porro laborum harum esse, nisi voluptates itaque vitae quis deleniti explicabo quam unde quas placeat eligendi nihil et animi nemo nulla ducimus? Dignissimos unde explicabo nobis eum quia voluptate dolorem vitae at culpa. Earum.</p>
          <div class="text-xs-right">
            <em>
              <small>&mdash; D. V. Dear</small>
            </em>
          </div>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary" nuxt to="/setting">Let's Go!</v-btn>
          <v-spacer />
        </v-card-actions>
        <v-container style="height: 30px;"></v-container>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";
import CardverseLogo from "~/components/CardverseLogo.vue";

export default {
  components: {
    Logo,
    VuetifyLogo,
    CardverseLogo
  }
};
</script>
