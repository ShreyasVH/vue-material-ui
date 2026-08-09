<template>
  <div class="search-select">
    <v-menu
        v-model="open"
        :close-on-content-click="false"
        location="bottom"
        :width="300"
    >
      <template #activator="{ props }">
        <v-text-field
            v-bind="props"
            v-model="search"
            label="Search"
            variant="outlined"
            hide-details
            autocomplete="off"
            @input="handleChange"
        />
      </template>

      <v-list v-if="options.length" max-height="250">
        <v-list-item
            v-for="item in options"
            :key="item"
            :title="item"
            @click="event => handleSelect(event, item)"
        />
      </v-list>
    </v-menu>
  </div>
</template>


<script>



export default {
  name: "SearchSelect",
  data() {
    return {
      search: "",
      open: false,
      options: []
    };
  },
  props: {
    onSelect:{
      type: Function
    }
  },
  methods: {
    async handleChange() {
      this.open = this.search.length >= 2;

      const keyword = event.target.value;
      if (keyword.length >= 2) {
        this.options = await this.searchItems(keyword);
        this.open = true;
      }
      this.search = keyword;
    },

    handleSelect(event, item) {
      console.log(item);
      this.onSelect && this.onSelect(event, item);
      this.open = false;
      this.search = '';
      this.options = [];
    },

    searchItems(keyword) {
      let options = [];
      if (keyword.length === 2) {
        options = [
          'Apple',
          'Orange'
        ];
      } else if (keyword.length === 3) {
        options = [
          'Banana',
          'Grapes'
        ];
      } else if (keyword.length === 4) {
        options = [
          'Pomegranate'
        ];
      }

      return options;
    }
  }
}
</script>

<style scoped>
.search-select {
  position: relative;
  width: 300px;
}

</style>