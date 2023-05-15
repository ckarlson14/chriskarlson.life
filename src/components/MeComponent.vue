<template>
  <div class="hello" :ref="'Chris Karlson'">
    <h5> Chris Karlson</h5>
    <p class="mt-3">
      I'm a self-taught software developer currently living in San Francisco who likes to build new things. I graduated from Brown University in 2018 with degrees in Engineering and Applied Math-Economics. Sometimes I <a class="pinkLink" href="https://chriskarlson.substack.com/" target="_blank"> write. </a> In my free time I like to take <a class="pinkLink" href="https://instagram.com/chrisfunpics" target="_blank"> pictures</a>, play, watch, and bet on sports, cook and eat food, and read books. If you're reading this, click <a class="pinkLink" href="#" v-on:click="this.sayHi"> here</a> to say hi.
    </p>
  </div>
</template>

<script>
export default {
  name: "MeComponent",
  methods: {
    sayHi: function() {
      window.alert('Hi back. Now do it in real life.')
    },
    scrollDown: function () {
      let element = document.getElementsByClassName('projects');
      if (element.length > 0){
        var top = element[0].offsetTop - 10;
        window.scrollTo(0, top);
      }
    }
  }
}
</script>

<style scoped>

h4{
  font-weight: 550 !important;
}

.hello{
  text-align: left;
  max-width: 70%;
  display: inline-flex;
  flex-wrap: wrap;
  color: black;
}

a{
  color: #e853e7;
  text-decoration: none;
}

a:hover{
  color:cyan;

}
</style>