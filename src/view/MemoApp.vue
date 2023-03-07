<template>
  <div>
    <formApp-component
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
    // // メモ入力画面の表示制御用
    // isFormVisible: false
    }
  },
  created () {},
  computed: {},
  methods: {}
}
</script>
