<template>
  <div class="containerProf">
    <div :class="['profile-image', shape]" :style="{width: size, height: size}">
      <img src="./assets/square.jpg">
    </div>
  </div>
  </template>
  
  <script>
  export default {
    props: {
      altText: {
        type: String,
        default: 'Profile Image',
      },
      size: {
        type: String,
        default: '50px',
      },
      shape: {
        type: String,
        default: 'square', // Can be 'circle' or 'square'
      },
    },
  };
  </script>
  
  <style>
  .containerProf{
    display: flex;
    justify-content: center;
  }
  .profile-image {
    display: flex;
    overflow: visible;
  }
  .circle img{
    border-radius: 50%;
  }
  .square img{
    border-radius: 10px;
    
  }
  </style>
  