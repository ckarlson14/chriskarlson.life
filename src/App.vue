<template>
  <div id="app">
    <MainHolder/>
  </div>
</template>

<script>
import MainHolder from './components/MainHolder.vue'

export default {
  name: 'App',
  components: {
    MainHolder
  }
}

</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Raleway&display=swap")

html, body {
  font-family: 'Raleway', sans-serif;
  background-color: whitesmoke;
}

#app {
  font-family: 'Raleway', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*display: inline-flex;*/
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}

h5{
  size: 2.5rem;
  margin-top: 8px !important;
  color: #e853e7;
  font-weight: 550 !important;
}

.titles{
  width:70%;
  text-align: left;
}



</style>
