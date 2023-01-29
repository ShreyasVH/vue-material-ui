<template>
  <div>
    <h2>
      Image:
    </h2>

    <div class="d-inline-flex flex-row justify-start">
      <v-avatar image="https://mui.com/static/images/avatar/1.jpg" />
      <v-avatar image="https://mui.com/static/images/avatar/1.jpg" size="80" rounded="0" />
    </div>

    <h2>
      Letter:
    </h2>

    <v-avatar color="grey">
      H
    </v-avatar>

    <v-avatar color="red">
      <span>N</span>
    </v-avatar>

    <h2>
      Icons:
    </h2>

    <v-avatar color="red">
      <v-icon icon="mdi-delete"></v-icon>
    </v-avatar>

    <v-avatar color="red" rounded="0">
      <v-icon icon="mdi-delete"></v-icon>
    </v-avatar>
  </div>
</template>

<script>
export default {
  name: "Avatars"
}
</script>

<style scoped>

</style>