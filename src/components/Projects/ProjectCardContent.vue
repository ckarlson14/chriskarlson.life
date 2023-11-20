<template>
  <div>
    <b-card-text class="logoLink body" :to="item.url" target="_blank">
      <img :src="item.logoFile" class="logo" />
      <!-- <span class="title">
          {{ item.name }}
          <SocialIcons :social="item.social" />
        </span> -->
      <span v-for="(social, i) in item.social" :key="i" class="m-1">
        <a :href="social.url" target="_blank" :class="social.icon"></a>
      </span>
    </b-card-text>
    <div class="text-muted ml-3 body">{{ item.description }}</div>
    <div class="card-text ml-3 body">{{ item.subtitle }}</div>
    <!-- <SkillList :skills="item.skills" /> -->
    <b-card-text>
      <ul class="projectSkills body">
        <li class="projectSkills" v-for="(item, key) in item.skills" :key="key">
          <i :class="item"></i>
        </li>
      </ul>
    </b-card-text>
  </div>
</template>

<script>
// import SocialIcons from "./SocialIcons.vue";
// import SkillList from "./SkillList.vue";

export default {
  components: {
    // SocialIcons,
    // SkillList,
  },
  props: {
    item: Object,
  },
};
</script>
