<template>
    <div class="card card-carousel overflow-hidden h-450 p-0">
      <div id="carouselExampleCaptions" class="carousel slide h-100" data-bs-ride="carousel">
        <div class="carousel-inner border-radius-lg h-100 mt-wc">
          <div
            class="carousel-item h-100 active"
            :style="{backgroundImage: 'url(' + require('@/assets/img/confusion-matrix.png') + ')',
            backgroundSize: 'contain', backgroundRepeat: ' no-repeat',}"
          >
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "carousel",
  };
  </script>
  