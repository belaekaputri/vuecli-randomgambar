
<template>
  <div id="app">
   <h1 class="display-6 text-center mb-3 text-muted">Daftar Pantai Pilihan</h1>
   <hr>
    <Buton v-on:ganti-pantai="gantiPantai" ></Buton>
    <article v-if="!selectedPantai" class="d-flex align-content-center justify-content-evenly  flex-wrap" >
           <Pantai v-for="(item,index) of pantai" v-bind:pantai="item" :key="item.id" :index="index" > </Pantai>
    </article>

    <article v-else  class="d-flex justify-content-center">
          <Pantai v-bind:pantai="selectedPantai" :index="0" > </Pantai>
    </article>
  </div>
</template>

<script>
import Buton from './components/ButtonTop.vue'
import Pantai from './components/DetailPantai.vue'

export default {
  components: {
    Buton,
    Pantai
  },
   name: 'App',
  data:function(){
    return{
      pantai:[
        {
          id:1,
         nama:'Pantai',
         type:'Indonesia',
         gambar:'p1.jpg'
        },
        {
         id:2,
         nama:'Pantai',
         type:'Brunei',
         gambar:'p2.jpg'
        },
        {
         id:3,
         nama:'Pantai ',
         type:'Palestina',
         gambar:'p3.jpg'
        },
        {
         id:4,
         nama:'Pantai ',
         type:'Turki',
         gambar:'p4.jpg'
        },
        {
         id:5,
         nama:'Pantai',
         type:'Arab',
         gambar:'p5.jpg'
        },
        {
         id:6,
         nama:'Pantai',
         type:'Malaysia',
         gambar:'p6.jpg'
        }
      ],
      selectedPantai:''
    }
},
methods:{
  gantiPantai:function(){
    this.selectedPantai=this.randomPantai()
  },
  randomPantai(){
    return this.pantai[Math.floor(Math.random() * this.pantai.length)]
  }

}
}
</script>

<style>
body{background-image: linear-gradient(-225deg, #E3FDF5 0%, #FFE6FA 100%);}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
