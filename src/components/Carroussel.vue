<template>
    <div class="carousel">
      <div class="carousel-inner" :style="{transform: `translateX(-${currentSlide * 100}%)`}">
        <div class="carousel-item" v-for="(image, index) in images" :key="index">
          <img :src="image" :alt="`Image ${index + 1}`" />
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Carroussel',
    data() {
      return {
        images: [
          '../../public/img/oui.jpg',
          '../../public/img/oui1.jpg',
          '../../public/img/rerere.jpg',
          '../../public/img/rezhjez.jpg',
          
        ],
        currentSlide: 0,
      };
    },
    mounted() {
      setInterval(() => {
        this.currentSlide = (this.currentSlide + 1) % this.images.length;
      }, 3000); // Changez cette valeur pour modifier la durée entre les diapositives (en millisecondes)
    },
  };
  </script>
  
  <style scoped>
  .carousel {
    width: 100%;
    overflow: hidden;
    position: relative;
    background-color: #c0c0c0;
    box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
    border: 2px solid #ffcc00;
    border-radius: 10px;
  }
  
  .carousel-inner {
    display: flex;
    transition: transform 1s ease;
    width: 100%;
    height: 100%;
  }
  
  .carousel-item {
    flex-shrink: 0;
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .carousel-item img {
    aspect-ratio: 4 / 3;
  width: 50%;
  height: 60%; /* Ajustez cette valeur pour définir la hauteur des images */
  object-fit: cover;
  border: 1px solid #ffcc00;
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
}
  </style>
  