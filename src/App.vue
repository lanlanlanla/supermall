<template>
  <div id="app">
    <router-view/>
    <main-tab-bar></main-tab-bar>
  </div>
</template>
<script>
import MainTabBar from './components/mainTabbar/MainTabbar'
export default {
  components: {
    MainTabBar
  }
}
</script>
<style>
  @import "./assets/css/base.css";
</style>
