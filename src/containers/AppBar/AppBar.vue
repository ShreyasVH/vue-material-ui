<template>
    <v-app-bar color="primary" absolute>
      <template v-slot:prepend>
        <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>
      </template>

      <template v-slot:append>

        <ThemeSelector />
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
import ThemeSelector from "../../components/ThemeSelector.vue";

export default {
  name: "AppBar",
  components: {
    ThemeSelector
  },
  data () {
    return {
      drawerOpen: false
    }
  },
  methods: {
    toggleDrawer () {
      this.drawerOpen = !this.drawerOpen;
    }
  }
}
</script>

<style scoped>

</style>