<template>
    <div class="container">
    <div class="link-groups">
      <ul>
        <li v-for="group in linkGroups" :key="group.id">
          <span>{{ group.title }}</span>
          <ul>
            <li v-for="link in group.links" :key="link.id">
              <a :href="link.url">{{ link.text }}</a>
            </li>
          </ul>
        </li>
      </ul>
    </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        linkGroups: [
          {
            id: 1,
            title: 'Group 1',
            links: [
              { id: 1, text: 'Link 1.1', url: '/link1' },
              { id: 2, text: 'Link 1.2', url: '/link2' }
            ]
          },
          {
            id: 2,
            title: 'Group 2',
            links: [
              { id: 3, text: 'Link 2.1', url: '/link3' },
              { id: 4, text: 'Link 2.2', url: '/link4' }
            ]
          }
        ]
      };
    }
  }
  </script>
  
  <style>
  .link-groups {
    /* styling for the link groups */
    display: flex;
  }
  .link-groups ul {
    list-style-type: none;
    padding: 0;
  }
  .link-groups li {
    margin-bottom: 10px;
  }
  </style>
  