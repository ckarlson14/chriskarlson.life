<template>
  <div align="center">
    <div class="titles mt-3">
      <h5>Languages and Frameworks</h5>
    </div>
    <ul class="icons">
      <li class="skills" v-for="(item, key) in this.skills" :key="key">
        <i :class="item"></i>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MySkills.vue",
  data() {
    return {
      skills: ["devicon-swift-plain-wordmark colored", "devicon-react-original-wordmark colored", "devicon-vuejs-plain-wordmark colored", "devicon-nodejs-plain-wordmark colored", "devicon-express-original-wordmark colored", "devicon-python-plain-wordmark colored", "devicon-flask-original-wordmark colored", "devicon-javascript-plain colored", "devicon-html5-plain-wordmark colored", "devicon-css3-plain-wordmark colored", "devicon-bootstrap-plain-wordmark colored", "devicon-jquery-plain-wordmark colored", "devicon-npm-original-wordmark colored", "devicon-yarn-plain-wordmark colored", "devicon-firebase-plain-wordmark colored", "devicon-mongodb-plain-wordmark colored", "devicon-sqlalchemy-original-wordmark colored", "devicon-postgresql-plain-wordmark colored", "devicon-heroku-plain-wordmark colored", "devicon-amazonwebservices-plain-wordmark colored", "devicon-redis-plain-wordmark colored", "devicon-socketio-original-wordmark colored", "devicon-java-plain-wordmark colored", "devicon-matlab-plain colored", "devicon-arduino-plain-wordmark colored", "devicon-vscode-plain-wordmark colored", "devicon-xcode-plain colored", "devicon-github-original-wordmark colored", "devicon-jira-plain-wordmark colored", "devicon-confluence-original-wordmark colored"]
    }
  }
}
</script>

<style scoped>
.icons {
  max-width: 70%;
  display: flex;
  flex-wrap: wrap;
  padding-left: 0px;
}

.skills {
  /*max-width: 50%;*/
  padding: 10px;
  font-size: 2rem;
  display: flex;
  flex-wrap: wrap;
}
</style>