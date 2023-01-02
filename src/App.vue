<template>
  
    <h1>{{title}}</h1>
    <p>Welcome...</p>
    <div v-if="showModal">
    <Modal  theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href=#>lick me</a>
        <a href=#>more info</a>
      </template>
      <h1>Sele noe on</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure repellendus enim in?</p>
    </Modal>
    </div>

    <div v-if="showModalTow">
    <Modal @close="toggleModalTow">
     <h1>News leter</h1>
      <p>Loremadipisicing elit. Iure repellendus enim in?</p>
    </Modal>
    </div>    
    <button @click.alt="toggleModal">click me with ALT</button>
    <button @click="toggleModalTwo">click</button>

</template>

<script lang="ts">
import modal from './components/modal.vue'
export default {
  name: 'App',
  components:{modal},
  data(){
    return {
      title: 'My first Vue happy app))',
      showModal: false,
      showModalTow: false,

    }
  },
methods: {
  toggleModal() {
    this.showModal = !this.showModal 
  },
   toggleModalTow() {
    this.showModalTow = !this.showModalTow
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
