<template>
    <div>
      <!-- Button to show the modal -->
      <button @click="showModal">Show Modal</button>
  
      <!-- Modal component -->
      <Modal :visible="isModalVisible" @close="closeModal">
        <p>This is the content of the modal.</p>
      </Modal>
    </div>
  </template>
  
  <script>
  import Modal from './ModalWindow.vue'; // Adjust the import path as necessary
  
  export default {
    components: {
      Modal
    },
    data() {
      return {
        isModalVisible: false
      };
    },
    methods: {
      showModal() {
        this.isModalVisible = true;
      },
      closeModal() {
        this.isModalVisible = false;
      }
    }
  };
  </script>
  