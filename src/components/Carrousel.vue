<script>
import foto1 from '@/assets/img/1ff956fe.png';
// import foto2 from '@/assets/img/DSC_4770.jpg';
// import foto3 from '@/assets/img/DSC_4786.jpg';
// import foto4 from '@/assets/img/DSC_4796.jpg';
// import foto5 from '@/assets/img/DSC_4811.jpg';
// import foto6 from '@/assets/img/DSC_4835.jpg';
// import foto7 from '@/assets/img/DSC_4840.jpg';
// import foto8 from '@/assets/img/DSC_4842.jpg';


export default {
  name: 'Carrousel',
  data() {
    return {
      foto1

    }
  }
}
</script>
<template>
  
  <div class="container_carrousel">
    <div id="carouselExampleFade" class="carousel slide carousel-fade carousel_photo" data-bs-ride="carousel" data-bs-interval="2500">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img :src="foto1" class="d-block w-100" alt="...">
      </div>
      <!-- <div class="carousel-item">
        <img :src="foto2" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img :src="foto3" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img :src="foto4" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img :src="foto5" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img :src="foto6" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img :src="foto7" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img :src="foto8" class="d-block w-100" alt="...">
      </div> -->
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
  
  </div>
</template>
<style>
.container_carrousel{
  width:100%;
  height:100%;
}
.carousel_photo{
  min-width: 100vw;
}

</style>