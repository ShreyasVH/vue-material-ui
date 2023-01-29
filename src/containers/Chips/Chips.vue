<template>
  <div class="d-flex flex-row justify-lg-space-around">
    <v-chip>
      Default
    </v-chip>

    <v-chip color="primary">
      Primary
    </v-chip>

    <v-chip color="secondary">
      Secondary
    </v-chip>

    <v-chip color="success">
      Success
    </v-chip>

    <v-chip color="success" variant="outlined" @click="handleClose" >
      Success
    </v-chip>

    <v-chip v-if="!deleted" color="success" variant="outlined" closable @click:close="deleted = true">
      Success
    </v-chip>
    <v-btn v-if="deleted" @click="deleted = false">Reset</v-btn>
  </div>
</template>

<script>
export default {
  name: "Chips",
  data () {
    return {
      deleted: false
    }
  },
  methods: {
    handleClose (event) {
      event.preventDefault();
      event.stopPropagation()
      event.cancelBubble();
    }
  }
}
</script>

<style scoped>

</style>