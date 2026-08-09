<template>
  <SearchSelect :on-select="handleSelect" />

  {{selectedItem}}
</template>


<script>
import SearchSelect from '../../components/SearchSelect.vue'

export default {
  name: "SearchSelectContainer",
  data () {
    return {
      selectedItem: ''
    };
  },
  components: {
    SearchSelect
  },
  methods: {
    handleSelect: function(event, item) {
      this.selectedItem = item;
    }
  }
}
</script>