<template>
  <div>
   <v-data-table
    :headers="headers"
    :items="items"
    hide-default-header
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
      headers: [
        { value: 'title' },
        { value: 'date' },
        { value: 'contents' }
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
  created () {},
  computed: {},
  methods: {}
}
</script>
