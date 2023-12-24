<template>
    <div class="container">
    <div class="navbar">
      <div class="brand">MyApp</div>
      <ul>
        <li v-for="link in links" :key="link.id">
          <a :href="link.url">{{ link.text }}</a>
        </li>
      </ul>
    </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        links: [
          { id: 1, text: 'Home', url: '/' },
          { id: 2, text: 'About', url: '/about' },
          { id: 3, text: 'Services', url: '/services' },
          // ... add more links as needed
        ]
      };
    }
  }
  </script>
  
  <style>
  .navbar {
    /* styling for the navbar */
  }
  .navbar .brand {
    font-size: 24px;
    font-weight: bold;
  }
  .navbar ul {
    list-style-type: none;
    padding: 0;
  }
  .navbar li {
    display: inline-block;
    margin-right: 20px;
  }
  </style>
  