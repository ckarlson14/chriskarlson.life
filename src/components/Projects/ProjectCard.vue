<template>
    <b-link :to="item.url" target="_blank">
      <b-card no-body class="mt-3 projects" style="display: inline-flex">
        <b-card-body>
          <ProjectCardContent :item="item" />
        </b-card-body>
      </b-card>
    </b-link>
  </template>
  
  <script>
  import ProjectCardContent from './ProjectCardContent.vue';
  
  export default {
    components: {
      ProjectCardContent
    },
    props: {
      item: Object
    }
  };
  </script>
  