<template>
    <div class="container">
    <img src="./assets/mortal-kombat-scorpion-burning-4q6cak0d3tt1fgrx.gif" :alt="altText" :width="width" :height="height" />
    </div>
  </template>
  
  <script>
  export default {
    props: {
      altText: {
        type: String,
        default: 'Image',
      },
      width: {
        type: [Number, String],
        default: '100%',
      },
      height: {
        type: [Number, String],
        default: 'auto',
      },
    },
  };
  </script>
  
  <style>
    .container img{
        width: 500px;
    }
  </style>
  