<template>
  <h1>{{ t }}</h1>
  <div v-show="showModal">
 <Modal :header="headertext" :text="text" :theme="theme" @closeM="toggleModal"/>
 </div>
 <br>
 <button @click="toggleModal" >Show Modal</button>
</template>

<script>
import Modal from "./components/Modal"
export default {
  components:{Modal},
  data() {
    return{
     t:"Hello Vue",
     headertext:"Sign Up For The Giveaway",
     text:"Just kidding you won't get anything you peasant!",
     theme:"sle",
     showModal:false,
    }
    
  },
  methods:{
    toggleModal(){
      this.showModal=!this.showModal
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
