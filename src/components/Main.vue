<template>
  <div class="hello">
    <div align="center" >
      <nav
          v-for="(item, index) in this.navItems"
          :key="index"
          class="top"
      >
        <a class="item top" v-on:click="scrollTo(item)">{{item}}</a>
      </nav>
    </div>
    <Me></Me>
    <Projects></Projects>
    <Skills></Skills>
    <Social></Social>
    <Footer></Footer>
  </div>
</template>

<script>
import Me from "@/components/Me";
import Projects from "@/components/Projects";
import Skills from "@/components/Skills";
import Social from "@/components/Social";
import Footer
  from "@/components/Footer";
export default {
  name: 'Main',
  components: {
    Me,
    Projects,
    Social,
    Skills,
    Footer
  },
  data() {
    return{
      navItems: ["projects", "skills", "social"]
    }
  },
  methods: {
    scrollTo: function (newWeek) {
      console.log("scroll to", newWeek)
      let element = document.getElementsByClassName(newWeek);
      if (element.length > 0){
        var top = element[0].offsetTop - 10;
        window.scrollTo(0, top);
      }
    }
},
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.top{
  display: inline-flex;
  max-width: 70%;
  flex-wrap: wrap;
}

a{
  padding: 10px;
  font-size: 1.5rem;
  color: #e853e7;
  text-decoration: none;
}

a:hover{
  color:cyan;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}
.hello{
  margin-top: 0px;
  background-color: whitesmoke;
}

</style>
