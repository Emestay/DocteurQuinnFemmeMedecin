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
          'https://lvdneng.rosselcdn.net/sites/default/files/dpistyles_v2/ena_16_9_extra_big/2021/12/12/node_1113088/54308687/public/2021/12/12/B9729320055Z.1_20211212163248_000%2BG1IJH64HT.1-0.jpg?itok=dB7A8p0i1639323174',
          'https://www.serieously.com/app/uploads/2022/03/collage-sans-titre-84-min-1.jpg',
          'https://tel.img.pmdstatic.net/fit/http.3A.2F.2Fprd2-bone-image.2Es3-website-eu-west-1.2Eamazonaws.2Ecom.2FTEL.2F2019.2F09.2F20.2F911f976b-9da5-45b9-8f7c-2120fff7a071.2Ejpeg/1200x800/quality/65/jane-seymour-incarnait-l-insoumise-docteur-michaela-quinn-entre-1993-et-1998.jpg',
          'https://www.uneseriedanecdotes.fr/wp-content/webpc-passthru.php?src=https://www.uneseriedanecdotes.fr/wp-content/uploads/2021/07/Docteur-Quinn-femme-medecin.jpg&nocache=1',
          'https://thumb.canalplus.pro/http/unsafe/1440x810/filters:quality(80)/img-hapi.canalplus.pro:80/ServiceImage/ImageID/104694941',
          
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
  