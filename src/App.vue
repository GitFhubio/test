<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <BasicComponent v-for="(name,index) in usernames" :username="name" :key="index" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import BasicComponent from './components/BasicComponent.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    BasicComponent
  },
  data:function(){
    return {usernames:['pippo','pluto','paperino']
  }}
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
