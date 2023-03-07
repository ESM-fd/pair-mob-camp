<template>
  <div>
    <formApp-component
      v-if="isFormVisible"
      :isNew='isNew'
      :memoData='memoData'
      @addMemo='addMemo'
    ></formApp-component>
    <List
      v-if="isListVisible"
      @addNewItem='addNewItem'
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
    addNewItem () {
      this.isFormVisible = true
      this.isListVisible = false
    }
  }
}
</script>
