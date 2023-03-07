<template>
  <div>
    <formApp-component
      :isNew='isNew'
      :memoData='memoData'
      @addMemo='addMemo'
    ></formApp-component>
  </div>
</template>

<script>
import FormApp from '../components/FormApp.vue'
export default {
  components: {
    'formApp-component': FormApp
  },
  data () {
    return {
      // 新規更新フラグ
      isNew: false,
      // メモデータ
      memoData: { title: '', memo: '' }
    // // メモ入力画面の表示制御用
    // isFormVisible: false
    }
  },
  created () {},
  computed: {},
  methods: {}
}
</script>
