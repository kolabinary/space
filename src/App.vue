<template>
  <div id="app">
    <router-view></router-view>
    <home></home>
    <Rigel></Rigel>
    <Join></Join>

  </div>
</template>

<script>

  import home from  './components/home.vue'
  import Rigel from './components/Rigel.vue'
  import Join from './components/form.vue'


export default {
  name: 'App',
  components: {
          home,
          Rigel,
          Join
  }
}
</script>

<style>



#app {
  /*font-family: 'Nunito Sans', sans-serif;*/
  font-family: 'TT Norms Pro', 'sans-serif';
  /*font-family: Avenir, Helvetica, Arial, sans-serif;*/
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  /*margin-top: 60px;*/
  padding: 0;
  margin: 0!important;
  box-sizing: border-box;
}
</style>
