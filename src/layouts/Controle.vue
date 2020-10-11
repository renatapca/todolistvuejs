<template>
  <q-layout view="hHh Lpr fFf" >
    <q-page-container>
      <!-- This is where pages get injected -->
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<style lang="stylus">
body{
  background-color: $primary;
}
</style>

<script>
export default {
  // name: 'LayoutName',

  data () {
    return {
    }
  }
}
</script>
