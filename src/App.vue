<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <transla/>
  </div>
</template>

<script>
import transla  from './components/HelloI18n'

export default {
  name: 'App',
  components: {
    transla
  },
  created(){
    const locale=localStorage.getItem("locale")
    
    if(locale){
      this.$i18n.locale=locale;
    } 
    else if(navigator.language){
      this.$i18n.locale=navigator.language.substring(0,2);
      }
    
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
