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
    <MeComponent></MeComponent>
    <MyProjects></MyProjects>
    <MySkills></MySkills>
    <SocialAccounts></SocialAccounts>
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>
import MeComponent from "@/components/MeComponent";
import MyProjects from "@/components/Projects/MyProjects";
import MySkills from "@/components/MySkills";
import SocialAccounts from "@/components/SocialAccounts";
import FooterComponent
  from "@/components/FooterComponent";
export default {
  name: 'MainHolder',
  components: {
    MeComponent,
    MyProjects,
    SocialAccounts,
    MySkills,
    FooterComponent
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
