<template>
  <div id="app">
    <Menu />
    <Lottery msg="Welcome to National Lottery"/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Lottery from './components/Lottery.vue';
import Menu from './components/Menu.vue';

export default Vue.extend({
  name: 'app',
  components: {
    Lottery,
    Menu
  }
});
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px 10px 0;
}

.menu {
  float: right;
}
</style>
