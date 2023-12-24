<template>
    <div class="input-groups">
      <div>
        <label>Personal Information</label>
        
        <div class="input-group">
          <button @click="fillName('@')" class="was"> @ </button>
          <input type="text" placeholder="Username" v-model="first">
        </div>
        
        <div class="input-group">
          <input type="email" placeholder="Email" v-model="email">
          <button @click="fillEmail('@gmail.com')" class="was"> @gmail.com </button>
        </div>
        
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        first: '',
        email: ''
      };
    },
    methods: {
      fillName(symbol) {
        this.first = symbol + this.first;
      },
      fillEmail(symbol) {
        this.email = this.email + symbol;
      }
    }
  }
  </script>
  
  <style>
  .input-groups {
    display: grid;
    justify-content: center;
    padding: 40px;
  }
  
  .input-group {
    margin-bottom: 10px;
    display: flex;
  }
  
  .input-group input{
    margin-bottom: 10px;
    padding: 5px;
  }
  </style>
  