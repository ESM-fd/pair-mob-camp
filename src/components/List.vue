<template>
  <div>
    <v-text-field
      v-model="search"
      append-icon="mdi-magnify"
      label="Search"
      single-line
      hide-details
      ></v-text-field>
    <v-data-table
      :headers="headers"
      :items="items"
      :search="search"
      hide-default-header
      hide-default-footer
      class="elevation-1"
    ></v-data-table>
  <v-row>
    <v-btn
      color="primary"
      fab
      small
      dark
      class="ml-auto"
      @click="addNewItem"
      >
      <v-icon>mdi-pencil</v-icon>
    </v-btn>
  </v-row>
  </div>
</template>

<script>
export default {
  data () {
    return {
      search: '',
      headers: [
        { value: 'title' },
        { value: 'date', filterable: false },
        { value: 'contents', filterable: false }
      ],
      items: [
        {
          title: '合宿の計画',
          date: '03/07',
          contents: 'ペアモブの練習する'
        }
      ]
    }
  },
  methods: {
    addNewItem () {
      this.$emit('addNewItem')
    }
  }
}
</script>
