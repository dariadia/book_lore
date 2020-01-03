<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" :clipped="clipped" fixed app>
      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" router exact>
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
    <v-sheet id="scrolling-techniques-6" class="overflow-y-auto" max-height="600">
      <v-content>
        <v-container>
          <nuxt />
        </v-container>
      </v-content>
    </v-sheet>
    <v-footer :fixed="fixed" app>
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
          title: "Start Here: Setting",
          to: "/setting"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Characters",
          to: "#"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Realms : Dimensions : Parallels",
          to: "#"
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Cardverse Lore"
    };
  }
};
</script>
