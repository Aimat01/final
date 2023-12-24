<template>
    <div class="container">
    <nav class="breadcrumb">
      <ul>
        <li v-for="(crumb, index) in breadcrumbs" :key="index">
          <span v-if="index !== breadcrumbs.length - 1">{{ crumb.label }} &gt; </span>
          <span v-else>{{ crumb.label }}</span>
        </li>
      </ul>
    </nav>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      items: {
        type: Array,
        required: true,
      },
    },
    computed: {
      breadcrumbs() {
        return this.items.map(item => ({
          label: item.label,
          link: item.link || null,
        }));
      },
    },
  };
  </script>
  
  <style scoped>

  .breadcrumb {
    margin: 10px 0;
  }
  
  ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
  }
  
  li {
    margin-right: 5px;
    font-size: 1em;
  }
  
  span {
    text-decoration: none;
    color: #3498db;
    font-weight: bold;
    transition: color 0.3s ease;
  }
  
  span:hover {
    color: #2980b9;
  }
  </style>