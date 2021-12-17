<template>
  <div align="center">
    <div class="titles">
      <h5>What I'm working on</h5>
    </div>
    <div v-for="(item, index) in this.projects"
          :key="index">
      <b-link :to="item.url" target="_blank">
        <b-card no-body style="display: inline-flex" class="mt-3 projects">
          <b-card-body>
            <b-card-text :to="item.url" class="logoLink body" target="_blank">
              <img :src="item.logoFile" class="logo">
              <span class="title">
                {{ item.name }}
              </span>
            </b-card-text>
            <div class="text-muted ml-3 body">{{ item.description }}</div>
            <div class="card-text ml-3 body">{{ item.subtitle }}</div>
            <b-card-text>
              <ul class="projectSkills body">
                <li class="projectSkills" v-for="(item, key) in item.skills" :key="key">
                  <i :class="item"></i>
                </li>
              </ul>
            </b-card-text>
          </b-card-body>
        </b-card>
      </b-link>
    </div>

  </div>
</template>

<script>
export default {
  name: "Projects.vue",
  data() {
    return{
      projects:  [{
        id: "1",
        status: "current",
        logoFile: "/assets/wewake.png",
        name: "weWake",
        subtitle: "Alarm clock for friends",
        site: "App Store",
        url: "https://apps.apple.com/us/app/wewake/id1495745797",
        description:
            "iOS app",
        skills: ["devicon-swift-plain-wordmark colored","devicon-python-plain-wordmark colored","devicon-flask-original-wordmark colored","devicon-sqlalchemy-original-wordmark colored","devicon-amazonwebservices-plain-wordmark colored","devicon-html5-plain-wordmark colored", "devicon-css3-plain-wordmark colored"]
      },
        {
          id: "2",
          status: "current",
          logoFile: "/assets/birthpay.png",
          name: "birthpay",
          subtitle: "Schedule gifts and birthday reminders",
          site: "App Store",
          url: "https://apps.apple.com/us/app/birthpay/id1575770355",
          description:
              "iOS app",
          skills: ["devicon-swift-plain-wordmark colored","devicon-python-plain-wordmark colored","devicon-flask-original-wordmark colored","devicon-heroku-plain-wordmark colored", "devicon-sqlalchemy-original-wordmark colored", "devicon-postgresql-plain-wordmark colored","devicon-redis-plain-wordmark colored","devicon-html5-plain-wordmark colored", "devicon-css3-plain-wordmark colored"]
        },
        {
          id: "3",
          status: "current",
          logoFile: "/assets/iNFTsta.png",
          name: "iNFTsta",
          subtitle: "Turn your Instagram posts into NFTs, for free",
          site: "",
          url: "https://www.inftsta.com",
          description:
              "Web3 Ethereum Dapp",
          skills: [ "devicon-python-plain-wordmark colored","devicon-flask-original-wordmark colored", "devicon-heroku-plain-wordmark colored", "devicon-facebook-plain colored", "devicon-html5-plain-wordmark colored", "devicon-css3-plain-wordmark colored", "devicon-bootstrap-plain-wordmark colored", "devicon-javascript-plain colored", "devicon-jquery-plain-wordmark colored", "devicon-sqlalchemy-original-wordmark colored", "devicon-postgresql-plain-wordmark colored"]
        },
        {
          id: "4",
          status: "current",
          logoFile: "/assets/potw.png",
          name: "playoftheweek",
          subtitle: "NCAA plays of the week",
          site: "",
          url: "https://playoftheweek.com",
          description:
              "Website",
          skills: ["devicon-vuejs-plain-wordmark colored", "devicon-yarn-plain-wordmark colored\"", "devicon-html5-plain-wordmark colored", "devicon-css3-plain-wordmark colored", "devicon-javascript-plain colored" ]
        },
        {
          id: "5",
          status: "current",
          logoFile: "/assets/gerseyz.png",
          name: "GERSEYZ",
          subtitle: "Golf Jerseys",
          site: "",
          url: "https://gerseyz.com",
          description:
              "Shopify Store",
          skills: ["fa fa-instagram"]
        },
        {
          id: "6",
          status: "current",
          logoFile: "/assets/openAll.png",
          name: "OpenAll",
          subtitle: "Open all your tabs from a folder in one click",
          site: "",
          url: "https://chrome.google.com/webstore/detail/openall/oggmebnpooffnoofbbcmgdogdpjcffpo?hl=en&authuser=1",
          description:
              "Chrome Extension",
          skills: ["devicon-google-plain-wordmark colored", "devicon-html5-plain-wordmark colored", "devicon-css3-plain-wordmark colored", "devicon-javascript-plain colored"]
        },
        {
          id: "7",
          status: "current",
          logoFile: "/assets/hackerComments.png",
          name: "HackerComments",
          subtitle: "Open a hackerNews articles comment section after clicking through to the page",
          site: "",
          url: "https://chrome.google.com/webstore/detail/hacker-comments/didaegjbjcalcoiiiioecmkcfchhjanc?hl=en&authuser=1",
          description:
              "Chrome Extension",
          skills: ["devicon-google-plain-wordmark colored", "devicon-html5-plain-wordmark colored", "devicon-css3-plain-wordmark colored", "devicon-javascript-plain colored"]
        },
      ]
    }
  },
}
</script>

<style scoped>

.title{
  font-size: 1.2rem;
  font-weight: 500;
}
.projects{
  width:70%;
}

.projects:hover{
  background-color: cyan;
}

img {
  padding: 5px;
}

.projectSkills {
  padding: 10px;
  font-size: 2rem;
  display: inline-flex;
}

.body{
  display: flex;
  flex-wrap: wrap;
  margin-left: 10px;
  color: black;
}

ul {
  list-style-type: none;
  margin-bottom: 0px;
}

.logo{
  max-height: 2rem;
  vertical-align: middle;
  border-radius: 25%;
}

.logo:hover{
  opacity: 0.7;
}

.logoLink{
  display: flex;
  align-items: center;
}

a{
  color: #e853e7;
  text-decoration: none;
}

a:hover{
  color:cyan;

}
</style>