<template>
  <div>
    <h2>
      Text:
    </h2>

    <div class="d-flex justify-start">
      <v-btn variant="text" color="primary" >
        Button
      </v-btn>

      <v-btn variant="text" color="secondary" >
        Button
      </v-btn>

      <v-btn variant="text" color="success" >
        Button
      </v-btn>

      <v-btn variant="text" color="error" >
        Button
      </v-btn>

      <v-btn class="primary--text" variant="text" color="warning" >
        Button
      </v-btn>

      <v-btn variant="text" color="info" >
        Button
      </v-btn>

      <v-btn variant="text" disabled>
        Button
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: "TextButtons"
}
</script>

<style scoped>

</style>