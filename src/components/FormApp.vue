<template>
  <div>
    <v-btn
      color="blue"
      dark
      @click="saveMemo()"
    >
      完了
    </v-btn>
    <v-btn
      color="blue"
      dark
      @click="deleteMemo()"
    >
      削除
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
      @click="saveMemo()"
    >
      <v-icon dark>mdi-plus</v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  props: [
    // 新規更新フラグ
    'isNew',
    // メモデータ
    'memoData'
  ],
  data () {
    return {}
  },
  methods: {
    saveMemo () {
      // TODO:データベースへの保存処理
      if (this.isNew) {
        // 登録関数を呼び出す
        console.log('登録するよ')
      } else {
        // 更新関数を呼び出す
        console.log('更新するよ')
      }
      // フォーム画面のクローズ
      this.$emit('saveMemo')
    },
    deleteMemo () {
      // TODO:データベースの削除処理
      console.log('削除するよ')
      // フォーム画面のクローズ
      this.$emit('deleteMemo')
    }
  }
}
</script>
