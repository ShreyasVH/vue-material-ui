<template>
  <div class="d-inline-flex flex-row">
    <v-checkbox color="primary" label="Primary" value="true" v-model="values" />
    <v-checkbox color="success" label="Success" value="true" v-model="values" />
    <v-checkbox color="error" label="Error" value="true" v-model="values" />
    <v-checkbox color="info" label="Info" value="true" v-model="values" />
    <v-checkbox color="warning" label="Warning" value="true" v-model="values" />
    <v-checkbox color="primary" label="Indeterminate" value="true" indeterminate v-model="values" />
    <v-checkbox color="error"  value="true" false-icon="mdi-heart-outline" true-icon="mdi-heart" />
  </div>
</template>

<script>
export default {
  name: "Checkboxes",
  data () {
    return {
      values: [
        'true'
      ]
    };
  }
}
</script>

<style scoped>

</style>