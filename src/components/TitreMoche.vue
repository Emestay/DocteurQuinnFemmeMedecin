<template>
    <h1 @click="reverseTitle" class="ugly-title">{{ title }}</h1>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const title = ref('Docteur Quinn, Femme médecin !');
  
      function reverseTitle() {
        title.value = title.value.split('').reverse().join('');
      }
  
      return {
        title,
        reverseTitle,
      };
    },
  };
  </script>
  
  <style scoped>
  .ugly-title {
    font-family: 'Comic Sans MS', sans-serif;
    font-size: 48px;
    text-align: center;
    color: #ff00ff;
    text-shadow: 3px 3px 0px #0000ff, 6px 6px 0px rgba(0, 0, 255, 0.4);
  }
  
  .ugly-title:hover {
    text-shadow: 3px 3px 0px #0000ff, -3px -3px 0px rgba(0, 0, 255, 0.4);
    cursor: pointer;
    transition: all 0.3s ease;
  }
  .ugly-title::selection{
    background-color: transparent;
  color: inherit;
  }
  </style>
  