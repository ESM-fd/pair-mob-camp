<template>
  <div>
    <v-btn
      color="blue"
      dark
      >
      完了
    </v-btn>
    <v-row v-for="memo in memoList" :key="memo.id">
      <v-text-field
        label="題目"
        type="input"
      ></v-text-field>
      <v-textarea
        label="メモ内容"
        name="input-7-1"
      ></v-textarea>
    </v-row>
    <v-btn
      dark
      small
      color="grey"
      class="ma-2"
      @click="addInput()"
    >
      <v-icon dark>mdi-plus</v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  data () {
    return {}
  },
  created () {},
  computed: {},
  methods: {}
}
</script>
