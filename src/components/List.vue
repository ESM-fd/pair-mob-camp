<template>
  <div>
   一覧表示するよ
   <v-data-table
    :headers="headers"
    :items="items"
    class="elevation-1"
  ></v-data-table>
  </div>
</template>

<script>
export default {
  data () {
    return {
      headers: [
        {
          text: 'Dessert (100g serving)',
          align: 'start',
          sortable: false,
          value: 'name'
        },
        // { text: 'タイトル', value: 'title' },
        { value: 'title' },
        { value: 'date' }
        // { text: 'Carbs (g)', value: 'carbs' },
        // { text: 'Protein (g)', value: 'protein' },
        // { text: 'Iron (%)', value: 'iron' }
      ],
      items: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: 1
        }
      ]
    }
  },
  created () {},
  computed: {},
  methods: {}
}
</script>
