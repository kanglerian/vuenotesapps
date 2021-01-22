<template>
  <div id="app">
    <h3 class="title">To Do List</h3>
    <div class="jobs">
      <div class="row justify-content-center">
       <div class="contaner">
        <div class="col-12">
         <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="job text-left">
           <ItemTugas v-bind:tugasSaya="tugasSaya" />
        </div>
      </div>
     
      </div>
      </div>
    </div>
  </div>
</template>

<script>

import 'bootstrap/dist/css/bootstrap.css';
import ItemTugas from './components/ItemTugas.vue';

export default {
  name: 'App',
  data: function(){
    return{
      tugas: [
        {
          id:1,
          namaTugas: "Membersihkan Toilet",
          isDone: false
        },
        {
          id:2,
          namaTugas: "Ngoding",
          isDone: true
        },
        {
          id:3,
          namaTugas: "Bikin Desain",
          isDone: false
        }
      ]
    }
  },
  components: {
    ItemTugas
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
.title {
  padding: 20px 15px;
  width: 50%;
  margin: auto;
  margin-bottom: 30px;
  background: rgb(2, 158, 2);
}
.item {
  font-size: 18px;
  margin-bottom:20px;
  text-align: left;
}
.item-completed{
  color:green;
}
</style>
