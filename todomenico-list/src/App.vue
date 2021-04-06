<template>
  <div id="app">
    <div class="logo">
      <img alt="Vue logo" src="./assets/logo.png" />
    </div>
    <h1>Ci sono {{taskList.length}} Task da completare</h1>
    <input
      type="text"
      @keyup.enter="addTask()"
      v-model="newTask"
      placeholder="Aggiungi un task"
    />
    <button @click="addTask" >Aggiungi</button>
    <TaskComponent
      v-for="(taskitem, index) in taskList"
      :task="taskitem"
      :key="index"
      v-on:delTask="delateTask(index)"
    />
  </div>
</template>

<script>
import TaskComponent from "./components/TaskComponent.vue";

export default {
  name: "App",
  components: {
    TaskComponent,
  },
  data() {
    return {
      newTask: "",
      taskList: [],
    };
  },
  methods: {
    addTask: function() {
      this.taskList.push(this.newTask);
      this.newTask = "";
    },
    delateTask: function(index){
      this.taskList = this.taskList.filter((el, i) =>  i !== index );
    }
  },
};
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
