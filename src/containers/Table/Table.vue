<template>
  <v-table style="text-align: center;">
    <thead>
      <th v-for="columnName in columns">
        {{columnName}}
      </th>
    </thead>

    <tbody>
      <tr v-for="row in rows">
        <td v-for="column in columns">
          {{row[column.toLowerCase()]}}
        </td>
      </tr>
    </tbody>
  </v-table>
</template>

<script>
export default {
  name: "Table",
  data () {
    return {
      columns: ['Country', 'Capital', 'Currency', 'Continent'],
      rows: [
        {
          country: 'India',
          capital: 'New Delhi',
          currency: 'Rupee',
          continent: 'Asia'
        },
        {
          country: 'United Kingdom',
          capital: 'London',
          currency: 'Pound',
          continent: 'Europe'
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>