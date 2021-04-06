<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <BasicComponent v-for="(name,index) in usernames" :username="name" :key="index" />
     <div  :style="{
     color:postColor }">
      <TestComponent v-for="post in posts" :post="post" :key="post.id"  v-on:color-text="postColor = 'blue'" v-on:color-text2="postColor = 'orange'"/>
      </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import BasicComponent from './components/BasicComponent.vue'
import TestComponent from './components/TestComponent.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    BasicComponent,
    TestComponent
  },
  data:function(){
    return {
      postColor:'red',
    postFontSize: 1,
      usernames:['pippo','pluto','paperino'],
       posts: [
      { id: 1, title: 'My journey with Vue',content:'Sono molto infelice'},
      { id: 2, title: 'Blogging with Vue',content:'Ma proprio tanto tanto' },
      { id: 3, title: 'Why Vue is so fun',content:'Mi manca Alfredo' }
    ]
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
