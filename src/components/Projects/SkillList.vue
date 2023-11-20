<template>
    <ul class="projectSkills body">
      <li
        class="projectSkills"
        v-for="(skill, key) in skills"
        :key="key"
      >
        <i :class="skill"></i>
      </li>
    </ul>
  </template>
  
  <script>
  export default {
    props: {
      skills: Array
    }
  };
  </script>
  