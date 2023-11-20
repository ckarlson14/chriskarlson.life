<template>
    <div>
      <div class="titles">
        <h5>{{ title }}</h5>
      </div>
      <div v-for="(item, index) in projects" :key="index">
        <ProjectCard :item="item" />
      </div>
    </div>
  </template>
  
  <script>
  import ProjectCard from './ProjectCard.vue';
  
  export default {
    components: {
      ProjectCard
    },
    props: {
      title: String,
      projects: Array
    }
  };
  </script>
  