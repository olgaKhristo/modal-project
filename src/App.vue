<template>
  <div>
    <h1>{{title}}</h1>
    <modal :header="header" :text="text" theme="sale"/>
    <input type="text" ref="name">
    <button @click="handleClick">click me</button>
  </div>
</template>

<script lang="ts">
import modal from './components/modal.vue'
export default {
  name: 'App',
  components:{modal},
  data(){
    return {
      title: 'My first Vue happy app))',
      header: 'sing up for giveaway',
      text: 'Greb one you have time'
    }
  },
methods: {
  handleClick() {
    
  
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
h1{
  border-bottom: 1px solid salmon;
  display:inline-block ;
  padding-bottom: 10px;
}
</style>
