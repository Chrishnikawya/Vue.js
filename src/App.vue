<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <p>{{inputData}}</p>
    <input type="text" v-model="inputData" />
    <button @click="onAddInputDataToList" >click the button</button>
    <ul> 
      <li v-for="element in inputDataArray" :key="element">{{element}}</li>
    </ul>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
    inputData:null,
    inputDataArray:[]
   };  
  },
  methods:{
    onAddInputDataToList(){
      this.inputDataArray.push(this.inputData);
      console.log("The list is",this.inputDataArray)
    }
  },
  components:{}
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
