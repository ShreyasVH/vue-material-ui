<template>
  <v-layout>
    <AppBar />
    <v-main>
      <v-container>
        <Tabs />
      </v-container>
    </v-main>
  </v-layout>
</template>

<script>

import Tabs from '@/containers/Tabs/Tabs.vue'
import AppBar from "./containers/AppBar/AppBar.vue";

export default {
  name: 'App',
  components: {
    AppBar,
    Tabs
  }
}
</script>

