<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" :clipped="clipped" fixed app>
      <v-list>
        <v-list-item
          @click.stop="drawer = !drawer"
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      style="z-index:3"
      @click.stop="drawer = !drawer"
      :clipped-left="clipped"
      :collapse="!collapseOnScroll"
      :collapse-on-scroll="collapseOnScroll"
      absolute
      scroll-target="#scrolling-techniques-6"
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-sheet id="scrolling-techniques-6" class="overflow-y-auto" max-height="650">
      <v-container>
        <nuxt />
      </v-container>
    </v-sheet>
    <v-footer fixed app>
      <span>&copy; dariadia 2020</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      collapseOnScroll: true,
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Start Here: Series",
          to: "/setting"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Characters",
          to: "/characters"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Realms : Dimensions : Parallels",
          to: "/realms"
        }
      ],
      miniVariant: false,
      title: "Cardverse Lore"
    };
  }
};
</script>
