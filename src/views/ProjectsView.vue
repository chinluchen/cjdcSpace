<template>
    <div>
      <h1>我的專案</h1>
      <p>這裡展示我的開發專案：</p>
  
      <ul>
        <li v-for="project in projects" :key="project.id">
          <a :href="project.link" target="_blank">{{ project.name }}</a>
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const projects = ref([
    { id: 1, name: '專案 1', link: 'https://github.com/chinluchen/project1' },
    { id: 2, name: '專案 2', link: 'https://github.com/chinluchen/project2' },
  ])
  </script>
  
  <style scoped>
  h1 {
    color: #333;
  }
  ul {
    list-style: none;
    padding: 0;
  }
  li {
    margin: 10px 0;
  }
  a {
    color: #007bff;
    text-decoration: none;
  }
  a:hover {
    text-decoration: underline;
  }
  </style>
  