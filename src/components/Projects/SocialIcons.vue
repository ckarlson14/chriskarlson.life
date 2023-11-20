<template>
    <span>
      <span v-for="(social, index) in social" :key="index" class="m-1">
        <a :href="social.url" target="_blank" :class="social.icon"></a>
      </span>
    </span>
  </template>
  
  <script>
  export default {
    props: {
      social: Array
    }
  };
  </script>
  
  <style>
  /* You can add specific styles for the social icons here */
  </style>
  