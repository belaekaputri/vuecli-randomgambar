<template>

<div class="card mb-3 me-3 shadow-lg" style="max-width: 540px;">
  <div class="row g-0">
    <div class="col-md-4">
      <img :src="gambar" class="img-fluid rounded-start" alt="gambar" >
    </div>
    <div class="col-md-8">
      <div class="card-body">
        <h5 class="card-title">{{ pantai. nama }}</h5>
        <p class="card-text"> {{ pantai.type }}</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.Tempora recusandae illum dolorum deleniti natus quae molestiae dolor doloremque, amet laudantium, eveniet ipsa sequi dolorem. </p>
        <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
      </div>
    </div>
  </div>
</div>

</template>

<script>
   export default{
       props:['pantai','index'],
       computed:{
           gambar:function(){
               return require('../assets/pantai/'+this.pantai.gambar)
           }
       }
   }

</script>