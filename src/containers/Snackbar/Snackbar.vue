<template>
  <v-btn color="primary" v-on:click="(event) => showSnackbar(event, { type: 'success', message: 'Success' })">
    Show Success
  </v-btn>
  &nbsp;
  <v-btn color="primary" v-on:click="(event) => showSnackbar(event, { type: 'error', message: 'Error' })">
    Show Error
  </v-btn>
  &nbsp;
  <v-btn color="primary" v-on:click="(event) => showSnackbar(event, { type: 'info', message: 'Info' })">
    Show Info
  </v-btn>
  &nbsp;
  <v-btn color="primary" v-on:click="(event) => showSnackbar(event, { type: 'warning', message: 'Warning' })">
    Show Warning
  </v-btn>

  <v-snackbar v-model="visible" :color="type" :timeout="5000">
    {{message}}

    <template v-slot:actions>
      <v-btn
          color="white"
          variant="text"
          @click="hideSnackbar"
      >
        Close
      </v-btn>
    </template>
  </v-snackbar>
</template>

<script>
export default {
  name: "Snackbar",
  data () {
    return {
      visible: false,
      message: '',
      type: ''
    }
  },
  mounted() {
    const that = this
    window.addEventListener('show-snackbar', function(event) {
      that.setLoaderValue(true)
      that.message = event.detail.message
      that.type = event.detail.type
    });

    window.addEventListener('hide-snackbar', function(event) {
      that.setLoaderValue(false)
    });
  },
  methods: {
    showSnackbar: function (event, data) {
      event.preventDefault();

      const myEvent = new CustomEvent('show-snackbar', { detail: { type: data.type, message: data.message } });
      window.dispatchEvent(myEvent);
    },

    hideSnackbar: function () {
      const myEvent = new CustomEvent('hide-snackbar', {});
      window.dispatchEvent(myEvent);
    },

    setLoaderValue: function (value) {
      this.visible = value
    }
  }
}
</script>

<style scoped>

</style>