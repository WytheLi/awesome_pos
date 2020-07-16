<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <!-- 左侧栏 -->
    <leftNav></leftNav>
    <!-- 主体区域 -->
    <div class="main">
      <router-view/>
    </div>
  </div>
</template>

<script>
import leftNav from '@/components/common/leftNav'
export default {
  name: 'App',
  components: {
    leftNav
  }
}
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    /* margin-top: 60px; */
  }
  .main {
    height: 100%;
    width: 95%;
    float: left;
    background-color: #EFF2F7;
    overflow: auto;
  }
</style>
