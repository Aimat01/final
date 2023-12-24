<template>
    <div class="container">
    <div class="nav-links">
      <ul>
        <li v-for="link in links" :key="link.id" :class="{ 'active': link.active }">
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
          { id: 1, text: 'Home', url: '/', active: true },
          { id: 2, text: 'About', url: '/about', active: false },
          { id: 3, text: 'Services', url: '/services', active: false },
          // ... add more links as needed
        ]
      };
    }
  }
  </script>
  
  <style>
  .nav-links {
    /* styling for the navigation links */
  }
  .nav-links ul {
    list-style-type: none;
    padding: 0;
  }
  .nav-links li {
    display: inline;
    margin-right: 10px;
  }
  .nav-links .active a {
    font-weight: bold;
  }
  </style>
  