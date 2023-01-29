<template>
  <div>
    <h2>
      Icon:
    </h2>

    <div class="d-flex flex-row align-center justify-space-around">
      <v-btn
        class="ma-2"
        variant="text"
        icon="mdi-delete"
        color="error"></v-btn>

      <v-btn color="primary" prepend-icon="mdi-delete" >
        Button
      </v-btn>

      <v-btn color="primary" append-icon="mdi-delete" >
        Button
      </v-btn>

      <v-btn variant="outlined" color="primary" prepend-icon="mdi-delete" >
        Button
      </v-btn>

      <v-btn variant="outlined" color="primary" append-icon="mdi-delete" >
        Button
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: "IconButtons"
}
</script>

<style scoped>

</style>