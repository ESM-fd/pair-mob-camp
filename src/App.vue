<template>
  <v-app id="app-root">
    <v-app-bar
      app
      dark
      color="primary"
    >
      <v-toolbar-title>
        メモ帳アプリ
      </v-toolbar-title>
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <memo-app />
      </v-container>
    </v-main>
  </v-app>
</template>

<script lang="js">
import Vue from 'vue'
import MemoApp from '@/view/MemoApp'

export default Vue.extend({
  components: {
    MemoApp
  },
  data () {
    return {}
  },
  created () {}
})
</script>
