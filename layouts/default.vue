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
                lazy-src="https://static3.seekingalpha.com/uploads/2020/2/18/28195863-15820538040943792_origin.png"
                src="https://static3.seekingalpha.com/uploads/2020/2/18/28195863-15820538040943792_origin.png"
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
