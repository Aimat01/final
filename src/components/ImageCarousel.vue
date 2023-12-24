<template>
    <div class="image-carousel">
      <div class="carousel-container">
          <img :src="images[currentIndex]" alt="Carousel Image" />
      </div>
      <button class="prev-btn" @click="prevImage">&#10094;</button>
      <button class="next-btn" @click="nextImage">&#10095;</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentIndex: 0,
      };
    },
    props: {
      images: {
        type: Array,
        required: true,
      },
    },
    methods: {
      nextImage() {
        this.currentIndex = (this.currentIndex + 1) % this.images.length;
      },
      prevImage() {
        this.currentIndex = (this.currentIndex - 1 + this.images.length) % this.images.length;
      },
    },
  };
  </script>
  
  <style scoped>
  
  
  .image-carousel {
    position: relative;
    overflow: hidden;
    width: 100%;
    max-width: 600px; 
    margin: 0 auto;
  }
  
  .carousel-container {
    display: flex;
    transition: transform 0.5s ease-in-out;
  }
  
  .carousel-item {
    flex: 0 0 100%;
  }
  
  img {
    width: 100%;
    height: auto;
    border-radius: 8px;
  }
  
  .prev-btn,
  .next-btn {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    font-size: 24px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 50%;
    padding: 10px;
    cursor: pointer;
    outline: none;
  }
  
  .prev-btn {
    left: 10px;
  }
  
  .next-btn {
    right: 10px;
  }
  </style>