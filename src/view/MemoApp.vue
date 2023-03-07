<template>
  <div>
    <formApp-component
      v-if="isFormVisible"
      :isNew='isNew'
      :memoData='memoData'
      @saveMemo='saveMemo'
      @deleteMemo='deleteMemo'
    ></formApp-component>
    <List
      v-if="isListVisible"
      @addNewItem='addNewItem'
      @modifyItem='modifyItem'
    ></List>
  </div>
</template>

<script>
import FormApp from '../components/FormApp.vue'
import List from '../components/List'
export default {
  components: {
    'formApp-component': FormApp,
    List
  },
  data () {
    return {
      // 新規更新フラグ
      isNew: false,
      // メモデータ
      memoData: { title: '', memo: '' },
      // メモ入力画面の表示制御用
      isFormVisible: false,
      isListVisible: false
    }
  },
  created () {
    this.isListVisible = true
  },
  methods: {
    // 新規登録ボタンのイベント
    addNewItem () {
      this.isFormVisible = true
      this.isListVisible = false
    },
    // 完了ボタンのイベント
    saveMemo () {
      this.isFormVisible = false
      this.isListVisible = true
    },
    // 削除ボタンのイベント
    deleteMemo () {
      this.isFormVisible = false
      this.isListVisible = true
    },
    // 行クリック編集のイベント
    modifyItem (row) {
      this.isFormVisible = true
      this.isListVisible = false
      this.memoData.title = row.title
      this.memoData.memo = row.contents
    }
  }
}
</script>
