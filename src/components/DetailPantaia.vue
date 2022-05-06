<template>
<div class="container">
<div class="row row-cols-1 row-cols-md-3 g-4 d-flex">
  <div class="col">
    <div class="card">
      <img :src="gambar" class="card-img-top w-25 h-25" alt="pantai">
      <div class="card-body">
        <h5 class="card-title">{{ pantai. nama }}</h5>
        <p class="card-text">{{ pantai.type }}</p>
      </div>
    </div>
  </div>
  </div>
  </div>
</template>

<script>
   export default{
       props:['pantai'],
       computed:{
           gambar:function(){
               return require('../assets/pantai/'+this.pantai.gambar)
           }
       }
   }

</script>