<template>
    <div class="container">
        <div v-if="visible" class="modal-overlay">
            <div class="modal-content">
                <span class="close-btn" @click="closeModal">&times;</span>
                <slot></slot>
            </div>
        </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      visible: {
        type: Boolean,
        required: true
      }
    },
    methods: {
      closeModal() {
        this.$emit('close');
      }
    }
  }
  </script>
  
  <style>
    .container{
        display: flex;
        justify-content: center;
        padding-top: 40px;
    }
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .modal-content {
    background-color: #fff;
    color: black;
    padding: 20px;
    border-radius: 4px;
    position: relative;
    width: 60%;
    max-width: 500px;
  }
  
  .close-btn {
    position: absolute;
    top: 10px;
    right: 10px;
    cursor: pointer;
    font-size: 24px;
    color: #aaa;
  }
  </style>
    