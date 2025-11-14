<template>
  <v-tabs v-model="value" color="primary">
    <v-tab key="Button">
      Buttons
    </v-tab>
    <v-tab key="Avatar">
      Avatars
    </v-tab>
    <v-tab key="Checkbox">
      Checkboxes
    </v-tab>
    <v-tab key="Chip">
      Chips
    </v-tab>
    <v-tab key="Table">
      Table
    </v-tab>
    <v-tab key="Loader">
      Loader
    </v-tab>
  </v-tabs>

  <v-window v-model="value">
    <v-window-item key="Button">
      <Buttons />
    </v-window-item>
    <v-window-item key="Avatar">
      <Avatars />
    </v-window-item>
    <v-window-item key="Checkbox">
      <Checkboxes />
    </v-window-item>
    <v-window-item key="Chip">
      <Chips />
    </v-window-item>
    <v-window-item key="Table">
      <Table />
    </v-window-item>
    <v-window-item key="Loader">
      <Loader />
    </v-window-item>
  </v-window>
</template>

<script>

import Buttons from '../Buttons/Buttons.vue';
import Avatars from '../Avatars/Avatars.vue';
import Checkboxes from '../Checkboxes/Checkboxes.vue';
import Chips from "../Chips/Chips.vue";
import Table from '../Table/Table.vue';
import Loader from '../Loader/Loader.vue';

export default {
  name: "Tabs",
  data () {
    return {
      value: 'Button'
    };
  },
  components: {
    Chips,
    Buttons,
    Avatars,
    Checkboxes,
    Table,
    Loader
  }
}
</script>

<style scoped>

</style>