<template>
  <v-app id="inspire">
      <v-spacer></v-spacer>
    <v-navigation-drawer v-model="drawer" app right>
      <v-list dense>
        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-home</v-icon>
          </v-list-item-action>

          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-email</v-icon>
          </v-list-item-action>

          <v-list-item-content>
            <v-list-item-title>Contact</v-list-item-title>
          </v-list-item-content><br>
           <v-toolbar-items class="hidden-sm-and-down">
            <v-btn>Login</v-btn>
          </v-toolbar-items>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app color="cyan" dark>
      <v-spacer></v-spacer>

      <v-toolbar-title>Application</v-toolbar-title>

      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
    </v-app-bar>

   

    <v-footer color="cyan" app>
      <v-spacer></v-spacer>

      <span class="white--text">&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "Page",
  props: {
    source: String
  },
  data: () => ({
    drawer: null
  })
};
</script>