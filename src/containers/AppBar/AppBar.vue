<template>
    <v-app-bar color="primary" absolute>
      <template v-slot:prepend>
        <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>
      </template>

      <template v-slot:append>

        <v-switch
            color="secondary"
            :label="mode === 'dark' ? 'Dark mode' : 'Light mode'"
            @change="toggleMode"
            v-model="isDark"
        ></v-switch>
      </template>
    </v-app-bar>

  <v-navigation-drawer
      v-model="drawerOpen"
      temporary
  >
    <v-list nav>
      <v-list-item title="Item 1" value="item1"></v-list-item>

      <v-list-item title="Item 2" value="item2"></v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
import { useTheme } from 'vuetify'

export default {
  name: "AppBar",
  setup() {
    const theme = useTheme();

    return {
      theme
    }
  },
  data () {
    const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
    return {
      drawerOpen: false,
      mode: prefersDark ? 'dark' : 'light'
    }
  },
  methods: {
    toggleDrawer () {
      this.drawerOpen = !this.drawerOpen;
    },

    toggleMode () {
      const newMode = this.mode === 'dark' ? 'light' : 'dark';
      this.mode = newMode;
      this.theme.change(newMode);
    }
  },
  computed: {
    isDark () {
      return this.mode === 'dark';
    }
  }
}
</script>

<style scoped>

</style>