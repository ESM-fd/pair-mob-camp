<template>
  <div>
    <v-btn
      color="blue"
      dark
      >
      完了
    </v-btn>
    <v-text-field
      label="題目"
      type="input"
      v-model="memoData.title"
    ></v-text-field>
    <v-textarea
      label="メモ内容"
      name="input-7-1"
      v-model="memoData.memo"
    ></v-textarea>
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
    return {
      memoData: { title: '', memo: '' }
    }
  },
  methods: {
    addInput () {
      // TODO:データベースへの保存処理
    }
  }
}
</script>
