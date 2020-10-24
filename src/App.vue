<template>
  <v-app>
    <v-navigation-drawer app v-model="drawer" clipped>navigation Lists</v-navigation-drawer>
    <v-app-bar color="primary" dark app clipped-left>
      <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>toolbar-title</v-toolbar-title>
      <v-spacer></v-spacer>

      <v-toolbar-items>
        <v-btn text>For Enterprise</v-btn>
        <v-menu offset-y>
          <template v-slot:activator="{on}">
            <v-btn v-on="on" text>Support</v-btn>
          </template>
          <v-list>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>Consulting and support</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>Discord community</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-menu>
        <!-- <v-btn outlined x-small>Button</v-btn>
        <v-btn text>Button</v-btn>
        <v-btn x-large>Button</v-btn>-->
      </v-toolbar-items>
    </v-app-bar>
    <v-footer color="primary" app>Footer</v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: null,
    };
  },
};
</script>