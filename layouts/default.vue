<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            <v-layout align-center>
              <v-img
                width="10"
                lazy-src="data:image/png;base64,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"
                src="data:image/png;base64,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"
              ></v-img>
              Pinterest
            </v-layout>
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>
      <v-divider></v-divider>

      <v-list dense nav class="mx-n1">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <div class="subtitle-2 grey--text mx-4">insights</div>
      <v-list dense nav class="mx-n1">
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-mail</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Messages</v-list-item-title>
          </v-list-item-content>

          <v-list-item-avatar color="red" size="20" class="white--text">
            1
          </v-list-item-avatar>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-bell</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>
              Notifications
            </v-list-item-title></v-list-item-content
          >

          <v-list-item-avatar size="20" color="deep-purple" class="white--text">
            2
          </v-list-item-avatar>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>mdi-{{ `chevron-${miniVariant ? "right" : "left"}` }}</v-icon>
      </v-btn>
      <v-btn icon @click.stop="clipped = !clipped">
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <v-btn icon @click.stop="fixed = !fixed">
        <v-icon>mdi-minus</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Home",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Recent",
          to: "/inspire",
        },
        {
          icon: "mdi-view-dashboard",
          title: "Following",
          to: "/modulos",
        },
      ],

      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
    };
  },
};
</script>
